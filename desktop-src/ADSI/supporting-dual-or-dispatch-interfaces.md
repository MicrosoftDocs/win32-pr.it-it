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
# <a name="supporting-dual-or-dispatch-interfaces"></a>Supporto di interfacce duali o dispatch

Analogamente all'interfaccia dispatch, tutte le interfacce duali devono ereditare da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), che delega tutte le relative funzioni **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) al **IDispatch** di Aggregator (ADSI). Per delegare, un oggetto estensione deve eseguire una query per il **IDispatch** di aggregator, chiamare il metodo aggregator appropriato e rilasciare il puntatore dopo l'utilizzo.

Se l'estensione può essere un componente autonomo, verificarne l'aggregazione. In tal caso, reindirizzare le funzioni di invio al [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) di aggregator. in caso contrario, è possibile chiamare l'implementazione interna di **IDispatch** oppure è possibile chiamare l'implementazione di [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

Nell'esempio di codice riportato di seguito viene illustrato come reindirizzare la chiamata [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a **IDispatch** di aggregator. Questo esempio di codice presuppone che la variabile membro **\_ pOuterUnknown** sia stata inizializzata al puntatore **IUnknown** di aggregator.


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



I writer di estensione sono vivamente invitati a supportare interfacce duali anziché interfacce dispatch negli oggetti di estensione. Una doppia interfaccia consente a un client di avere un accesso più veloce, purché l'accesso vtable sia abilitato nel client. Per ulteriori informazioni, vedere [associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md). In base al modello corrente, l'implementazione di interfacce duali non dovrebbe essere più difficile rispetto all'implementazione di interfacce dispatch.

 

 