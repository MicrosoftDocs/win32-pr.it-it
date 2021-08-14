---
title: Codice di esempio per l'individuazione di un servizio tramite una query RnR
description: L'esempio di codice seguente individua il servizio Winsock di esempio e vi si connette.
ms.assetid: c05c7f69-d510-4feb-b426-1ae3a3ed5e16
ms.tgt_platform: multiple
keywords:
- Codice di esempio per l'individuazione di un servizio tramite una query RnR ad AD
- Windows Registrazione dei socket e risoluzione di AD , codice di esempio, individuazione di un servizio tramite una query RnR
- Individuazione di un servizio tramite una query RnR ad , codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 076bf1cbd2c421c9d76b595a381f2884a398c0db42002e9deedfdd2e5084095d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191378"
---
# <a name="example-code-for-locating-a-service-using-an-rnr-query"></a>Codice di esempio per l'individuazione di un servizio tramite una query RnR

L'esempio di codice seguente individua il servizio Winsock di esempio e vi si connette.


```C++
#include "stdafx.h"
#include "shlobj.h"
#include "dsclient.h"


//  The PrintDomain() function displays the domain name.
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

//  The WalkDomainTree() function prints the current domain name and walks the tree.
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

//  Entry point for the application.
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



 

 




