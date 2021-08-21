---
title: Associazione a oggetti figlio
description: In ADSI un oggetto contenitore espone l'interfaccia IADsContainer.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , tramite, associazione a oggetti figlio
- Associazione a oggetti figlio
- oggetti figlio, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e454da1aaea93acc404e92da4b9c45ac8d67b4c3cee8a4fe9a04027c7533b39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429038"
---
# <a name="binding-to-child-objects"></a>Associazione a oggetti figlio

In ADSI un oggetto contenitore espone [**l'interfaccia IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Il [**metodo IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) viene usato per eseguire l'associazione direttamente a un oggetto figlio. L'oggetto restituito **da IADsContainer::GetObject** ha lo stesso contesto di sicurezza dell'oggetto su cui è stato chiamato il metodo. Ciò significa che se vengono usate credenziali alternative, non è necessario passare nuovamente le credenziali alternative alla funzione o al metodo di associazione per mantenere le stesse credenziali.

Il [**metodo IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) accetta un nome distinto relativo (RDN) relativo all'oggetto corrente. Questo metodo accetta anche un nome di classe facoltativo e restituisce un puntatore a interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che rappresenta l'oggetto figlio. Per ottenere l'interfaccia ADSI desiderata, ad esempio [**IAD,**](/windows/desktop/api/Iads/nn-iads-iads)chiamare il [**metodo QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di questo **puntatore a interfaccia IDispatch.**

Nell'esempio di codice C++ seguente viene illustrata una funzione che recupera un oggetto figlio specificato.


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 