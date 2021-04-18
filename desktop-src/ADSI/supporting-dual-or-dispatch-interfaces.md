---
title: Supporto di interfacce duali o dispatch
description: Analogamente all'interfaccia dispatch, tutte le interfacce duali devono ereditare da IDispatch, che delega tutte le relative funzioni IDispatch (GetIDsOfNames, Invoke, GetTypeInfo, GetTypeInfoCount) al IDispatch di Aggregator (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Supporto delle interfacce dual o dispatch ADSI
- estensioni ADSI, dual o dispatch Interface
- ADSI ADSI, esempio di codice C/C++, delega di metodi IDispatch a aggregator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435a4552b364afbf909d04a759e3713ce69befab
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300432"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a><span data-ttu-id="eb998-106">Supporto di interfacce duali o dispatch</span><span class="sxs-lookup"><span data-stu-id="eb998-106">Supporting Dual or Dispatch Interfaces</span></span>

<span data-ttu-id="eb998-107">Analogamente all'interfaccia dispatch, tutte le interfacce duali devono ereditare da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), che delega tutte le relative funzioni **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) al **IDispatch** di Aggregator (ADSI).</span><span class="sxs-lookup"><span data-stu-id="eb998-107">Like the dispatch interface, all dual interfaces must inherit from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), which delegates all of its **IDispatch** functions ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) back to the **IDispatch** of the aggregator (ADSI).</span></span> <span data-ttu-id="eb998-108">Per delegare, un oggetto estensione deve eseguire una query per il **IDispatch** di aggregator, chiamare il metodo aggregator appropriato e rilasciare il puntatore dopo l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="eb998-108">In order to delegate, an extension object should query for the **IDispatch** of the aggregator, call the appropriate aggregator method, and release the pointer after use.</span></span>

<span data-ttu-id="eb998-109">Se l'estensione può essere un componente autonomo, verificarne l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="eb998-109">If the extension can be a standalone component, verify that it is aggregated.</span></span> <span data-ttu-id="eb998-110">In tal caso, reindirizzare le funzioni di invio al [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) di aggregator. in caso contrario, è possibile chiamare l'implementazione interna di **IDispatch** oppure è possibile chiamare l'implementazione di [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="eb998-110">If so, reroute the dispatch functions to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) of the aggregator, otherwise you can call your internal implementation of **IDispatch**, or you can call your implementation of [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

<span data-ttu-id="eb998-111">Nell'esempio di codice riportato di seguito viene illustrato come reindirizzare la chiamata [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a **IDispatch** di aggregator.</span><span class="sxs-lookup"><span data-stu-id="eb998-111">The following code example shows how to reroute the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) call to the **IDispatch** of the aggregator.</span></span> <span data-ttu-id="eb998-112">Questo esempio di codice presuppone che la variabile membro **\_ pOuterUnknown** sia stata inizializzata al puntatore **IUnknown** di aggregator.</span><span class="sxs-lookup"><span data-stu-id="eb998-112">This code example assumes that the **m\_pOuterUnknown** member variable has been initialized to the **IUnknown** pointer of the aggregator.</span></span>


```C++
/////////////////////////////////////////////////// 
// Delegating IDispatch Methods to the aggregator
///////////////////////////////////////////////////
STDMETHODIMP MyExtension::GetTypeInfoCount(UINT* pctinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfoCount( pctinfo );
        pDisp->Release();
    }
    return hr;
}
 
 
STDMETHODIMP MyExtension::GetTypeInfo(UINT itinfo, LCID lcid, ITypeInfo** pptinfo)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetTypeInfo( itinfo, lcid, pptinfo );
        pDisp->Release();
    }
    
    return hr;
}
 
STDMETHODIMP MyExtension::GetIDsOfNames(REFIID riid, LPOLESTR* rgszNames, UINT cNames, LCID lcid, DISPID* rgdispid)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->GetIDsOfNames( riid, rgszNames, cNames, lcid, 
                 rgdispid);
        pDisp->Release();
    }
    
    return hr;
 
}
 
STDMETHODIMP MyExtension::Invoke(DISPID dispidMember, REFIID riid,
        LCID lcid, WORD wFlags, DISPPARAMS* pdispparams, VARIANT* 
                pvarResult, EXCEPINFO* pexcepinfo, UINT* puArgErr)
{
    IDispatch *pDisp = NULL;
    HRESULT    hr = S_OK;
    hr = m_pOuterUnknown->QueryInterface( IID_IDispatch, (void**) &pDisp );
    if ( SUCCEEDED(hr) )
    {
        hr = pDisp->Invoke( dispidMember, riid, lcid, wFlags, 
                 pdispparams, pvarResult, pexcepinfo, puArgErr);
        pDisp->Release();
    }
    
    return hr;
}
```



<span data-ttu-id="eb998-113">I writer di estensione sono vivamente invitati a supportare interfacce duali anziché interfacce dispatch negli oggetti di estensione.</span><span class="sxs-lookup"><span data-stu-id="eb998-113">Extension writers are strongly encouraged to support dual interfaces instead of dispatch interfaces in their extension objects.</span></span> <span data-ttu-id="eb998-114">Una doppia interfaccia consente a un client di avere un accesso più veloce, purché l'accesso vtable sia abilitato nel client.</span><span class="sxs-lookup"><span data-stu-id="eb998-114">A dual interface enables a client to have faster access, as long as vtable access is enabled in the client.</span></span> <span data-ttu-id="eb998-115">Per ulteriori informazioni, vedere [associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span><span class="sxs-lookup"><span data-stu-id="eb998-115">For more information, see [Late Binding vs. Vtable Access in the ADSI Extension Model](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).</span></span> <span data-ttu-id="eb998-116">In base al modello corrente, l'implementazione di interfacce duali non dovrebbe essere più difficile rispetto all'implementazione di interfacce dispatch.</span><span class="sxs-lookup"><span data-stu-id="eb998-116">Based on the current model, implementing dual interfaces should not be more difficult than implementing dispatch interfaces.</span></span>

 

 