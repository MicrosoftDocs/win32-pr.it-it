---
title: Associazione a oggetti figlio
description: In ADSI un oggetto contenitore espone l'interfaccia IADsContainer.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, associazione a oggetti figlio
- Associazione a oggetti figlio
- Oggetti figlio, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474211"
---
# <a name="binding-to-child-objects"></a><span data-ttu-id="491cd-106">Associazione a oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="491cd-106">Binding to Child Objects</span></span>

<span data-ttu-id="491cd-107">In ADSI un oggetto contenitore espone l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="491cd-107">In ADSI, a container object exposes the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span> <span data-ttu-id="491cd-108">Il metodo [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) viene usato per eseguire il binding diretto a un oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="491cd-108">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method is used to bind directly to a child object.</span></span> <span data-ttu-id="491cd-109">L'oggetto restituito da **IADsContainer:: GetObject** ha lo stesso contesto di sicurezza dell'oggetto sul quale è stato chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="491cd-109">The object returned by **IADsContainer::GetObject** has the same security context as the object on which the method was called.</span></span> <span data-ttu-id="491cd-110">Ciò significa che se vengono utilizzate credenziali alternative, non è necessario passare le credenziali alternative alla funzione o al metodo di associazione per mantenere le stesse credenziali.</span><span class="sxs-lookup"><span data-stu-id="491cd-110">This means that if alternate credentials are used, the alternate credentials do not have to be passed to the binding function or method again to maintain the same credentials.</span></span>

<span data-ttu-id="491cd-111">Il metodo [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) accetta un nome distinto relativo (RDN) relativo all'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="491cd-111">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method takes a relative distinguished name (RDN) that is relative to the current object.</span></span> <span data-ttu-id="491cd-112">Questo metodo accetta inoltre un nome di classe facoltativo e restituisce un puntatore a interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che rappresenta l'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="491cd-112">This method also takes an optional class name and returns an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface pointer that represents the child object.</span></span> <span data-ttu-id="491cd-113">Per ottenere l'interfaccia ADSI desiderata, ad esempio [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), chiamare il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del puntatore a interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="491cd-113">To obtain the desired ADSI interface, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of this **IDispatch** interface pointer.</span></span>

<span data-ttu-id="491cd-114">Nell'esempio di codice C++ riportato di seguito viene illustrata una funzione che recupera un oggetto figlio specificato.</span><span class="sxs-lookup"><span data-stu-id="491cd-114">The following C++ code example shows a function that retrieves a specified child object.</span></span>


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



 

 