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
# <a name="domain-browser"></a>Browser di dominio

Utilizzando l'interfaccia [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , un'applicazione può visualizzare una finestra di dialogo del browser del dominio e ottenere il nome DNS del dominio selezionato dall'utente. Un'applicazione può anche usare l'interfaccia **IDsBrowseDomainTree** per ottenere dati su tutti i domini e gli alberi di dominio all'interno di una foresta.

Un'istanza dell'interfaccia [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) viene creata chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe **CLSID \_ DsDomainTreeBrowser** come illustrato di seguito.

Il metodo [**IDsBrowseDomainTree:: secomputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) può essere utilizzato per specificare il computer e le credenziali utilizzate come base per il recupero dei dati del dominio. Quando viene chiamato il metodo **ToComputer** su una particolare istanza di [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) , [**IDsBrowseDomainTree:: FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) deve essere chiamato prima di chiamare di nuovo il **computer** .

Il metodo [**IDsBrowseDomainTree:: BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) viene utilizzato per visualizzare la finestra di dialogo del browser del dominio. Quando l'utente seleziona un dominio e fa clic sul pulsante **OK** , **IDsBrowseDomainTree:: BrowseTo** restituisce **S \_ OK** e il parametro *ppszTargetPath* contiene il nome del dominio selezionato. Quando la stringa del nome non è più necessaria, il chiamante deve liberare la stringa chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

Nell'esempio di codice seguente viene illustrato come utilizzare l'interfaccia [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) per visualizzare la finestra di dialogo Domain browser.


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



Il metodo [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) viene usato per ottenere i dati dell'albero del dominio. I dati del dominio sono forniti in una struttura [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) . La struttura **DOMAINTREE** contiene le dimensioni della struttura e il numero di elementi di dominio nell'albero. La struttura **DOMAINTREE** contiene anche una o più strutture [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) . **DOMAINDESC** contiene i dati relativi a un singolo elemento nell'albero del dominio, inclusi i dati figlio e di pari livello. Gli elementi di pari livello di un dominio possono essere enumerati accedendo al membro **pdNextSibling** di ogni struttura **DOMAINDESC** successiva. Gli elementi figlio del dominio possono essere recuperati in modo analogo accedendo al membro **pdChildList** di ogni struttura **DOMAINDESC** successiva.

Nell'esempio di codice seguente viene illustrato come ottenere e accedere ai dati dell'albero del dominio usando il metodo [**IDsBrowseDomainTree:: Getdomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) .


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



 

 