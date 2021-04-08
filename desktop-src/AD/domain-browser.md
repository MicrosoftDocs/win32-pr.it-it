---
title: Browser di dominio
description: Utilizzando l'interfaccia IDsBrowseDomainTree, un'applicazione può visualizzare una finestra di dialogo del browser del dominio e ottenere il nome DNS del dominio selezionato dall'utente.
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- Active Directory Domain browser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046517"
---
# <a name="domain-browser"></a><span data-ttu-id="93106-104">Browser di dominio</span><span class="sxs-lookup"><span data-stu-id="93106-104">Domain Browser</span></span>

<span data-ttu-id="93106-105">Utilizzando l'interfaccia [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , un'applicazione può visualizzare una finestra di dialogo del browser del dominio e ottenere il nome DNS del dominio selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="93106-105">Using the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface, an application can display a domain browser dialog box and obtain the DNS name of the domain selected by the user.</span></span> <span data-ttu-id="93106-106">Un'applicazione può anche usare l'interfaccia **IDsBrowseDomainTree** per ottenere dati su tutti i domini e gli alberi di dominio all'interno di una foresta.</span><span class="sxs-lookup"><span data-stu-id="93106-106">An application can also use the **IDsBrowseDomainTree** interface to obtain data about all domain trees and domains within a forest.</span></span>

<span data-ttu-id="93106-107">Un'istanza dell'interfaccia [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) viene creata chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe **CLSID \_ DsDomainTreeBrowser** come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="93106-107">An instance of the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface is created by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsDomainTreeBrowser** class identifier as shown below.</span></span>

<span data-ttu-id="93106-108">Il metodo [**IDsBrowseDomainTree:: secomputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) può essere utilizzato per specificare il computer e le credenziali utilizzate come base per il recupero dei dati del dominio.</span><span class="sxs-lookup"><span data-stu-id="93106-108">The [**IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) method can be used to specify which computer and credentials are used as the basis for retrieving the domain data.</span></span> <span data-ttu-id="93106-109">Quando viene chiamato il metodo **ToComputer** su una particolare istanza di [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , [**IDsBrowseDomainTree:: FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) deve essere chiamato prima di chiamare di nuovo il **computer** .</span><span class="sxs-lookup"><span data-stu-id="93106-109">When **SetComputer** is called on a particular [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) instance, [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) must be called before **SetComputer** is called again.</span></span>

<span data-ttu-id="93106-110">Il metodo [**IDsBrowseDomainTree:: BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) viene utilizzato per visualizzare la finestra di dialogo del browser del dominio.</span><span class="sxs-lookup"><span data-stu-id="93106-110">The [**IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) method is used to display the domain browser dialog box.</span></span> <span data-ttu-id="93106-111">Quando l'utente seleziona un dominio e fa clic sul pulsante **OK** , **IDsBrowseDomainTree:: BrowseTo** restituisce **S \_ OK** e il parametro *ppszTargetPath* contiene il nome del dominio selezionato.</span><span class="sxs-lookup"><span data-stu-id="93106-111">When the user selects a domain and clicks the **OK** button, the **IDsBrowseDomainTree::BrowseTo** returns **S\_OK** and the *ppszTargetPath* parameter contains the name of the selected domain.</span></span> <span data-ttu-id="93106-112">Quando la stringa del nome non è più necessaria, il chiamante deve liberare la stringa chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="93106-112">When the name string is no longer required, the caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

<span data-ttu-id="93106-113">Nell'esempio di codice seguente viene illustrato come utilizzare l'interfaccia [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) per visualizzare la finestra di dialogo Domain browser.</span><span class="sxs-lookup"><span data-stu-id="93106-113">The following code example shows how to use the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface to display the domain browser dialog box.</span></span>


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



<span data-ttu-id="93106-114">Il metodo [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) viene usato per ottenere i dati dell'albero del dominio.</span><span class="sxs-lookup"><span data-stu-id="93106-114">The [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method is used to obtain domain tree data.</span></span> <span data-ttu-id="93106-115">I dati del dominio sono forniti in una struttura [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) .</span><span class="sxs-lookup"><span data-stu-id="93106-115">The domain data is supplied in a [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) structure.</span></span> <span data-ttu-id="93106-116">La struttura **DOMAINTREE** contiene le dimensioni della struttura e il numero di elementi di dominio nell'albero.</span><span class="sxs-lookup"><span data-stu-id="93106-116">The **DOMAINTREE** structure contains the size of the structure and the number of domain elements in the tree.</span></span> <span data-ttu-id="93106-117">La struttura **DOMAINTREE** contiene anche una o più strutture [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) .</span><span class="sxs-lookup"><span data-stu-id="93106-117">The **DOMAINTREE** structure also contains one or more [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) structures.</span></span> <span data-ttu-id="93106-118">**DOMAINDESC** contiene i dati relativi a un singolo elemento nell'albero del dominio, inclusi i dati figlio e di pari livello.</span><span class="sxs-lookup"><span data-stu-id="93106-118">The **DOMAINDESC** contains data about a single element in the domain tree, including child and sibling data.</span></span> <span data-ttu-id="93106-119">Gli elementi di pari livello di un dominio possono essere enumerati accedendo al membro **pdNextSibling** di ogni struttura **DOMAINDESC** successiva.</span><span class="sxs-lookup"><span data-stu-id="93106-119">The siblings of a domain can be enumerated by accessing the **pdNextSibling** member of each subsequent **DOMAINDESC** structure.</span></span> <span data-ttu-id="93106-120">Gli elementi figlio del dominio possono essere recuperati in modo analogo accedendo al membro **pdChildList** di ogni struttura **DOMAINDESC** successiva.</span><span class="sxs-lookup"><span data-stu-id="93106-120">The children of the domain can be retrieved in a similar manner by accessing the **pdChildList** member of each subsequent **DOMAINDESC** structure.</span></span>

<span data-ttu-id="93106-121">Nell'esempio di codice seguente viene illustrato come ottenere e accedere ai dati dell'albero del dominio usando il metodo [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) .</span><span class="sxs-lookup"><span data-stu-id="93106-121">The following code example shows how to obtain and access the domain tree data using the [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method.</span></span>


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;

    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);

        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                           dwIndentLevel + 1);
        }
    }
}

//  Entry point for application
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;
        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        pBrowseTree->Release();
    }
    CoUninitialize();
}
```



 

 