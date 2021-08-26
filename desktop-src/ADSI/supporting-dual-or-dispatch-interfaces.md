---
title: Supporto di interfacce duali o dispatch
description: Analogamente all'interfaccia dispatch, tutte le interfacce duali devono ereditare da IDispatch, che delega tutte le funzioni IDispatch (GetIDsOfNames, Invoke, GetTypeInfo, GetTypeInfoCount) a IDispatch dell'aggregatore (ADSI).
ms.assetid: abd0fcfc-f45c-4022-af95-60615be0adcc
ms.tgt_platform: multiple
keywords:
- Supporto di interfacce duali o dispatch ADSI
- estensioni ADSI, interfacce duali o dispatch
- ADSI ADSI , codice di esempio C/C++, delega dei metodi IDispatch all'aggregatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b783e9448926d6d29a27e5fb0db519175f82a9af1935e9f13655db743a946bcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930011"
---
# <a name="supporting-dual-or-dispatch-interfaces"></a>Supporto di interfacce duali o dispatch

Analogamente all'interfaccia dispatch, tutte le interfacce duali devono ereditare da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), che delega tutte le relative funzioni **IDispatch** ([**GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames), [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke), [**GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo), [**GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount)) a **IDispatch** dell'aggregatore (ADSI). Per delegare, un oggetto di estensione deve eseguire una query **per IDispatch** dell'aggregatore, chiamare il metodo dell'aggregatore appropriato e rilasciare il puntatore dopo l'uso.

Se l'estensione può essere un componente autonomo, verificare che sia aggregata. In tal caso, reindirizzare le funzioni di invio [**all'oggetto IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) dell'aggregatore, in caso contrario è possibile chiamare l'implementazione interna di **IDispatch** oppure è possibile chiamare l'implementazione di [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

Nell'esempio di codice seguente viene illustrato come reindirizzare la chiamata [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **all'oggetto IDispatch** dell'aggregatore. Questo esempio di codice presuppone che la variabile membro **m \_ pOuterUnknown** sia stata inizializzata sul puntatore **IUnknown** dell'aggregatore.


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



I writer di estensioni sono fortemente invitati a supportare le interfacce duali anziché le interfacce dispatch nei relativi oggetti di estensione. Una doppia interfaccia consente a un client di avere un accesso più rapido, purché l'accesso vtable sia abilitato nel client. Per altre informazioni, vedere [Associazione tardiva e Accesso Vtable nel modello di estensione ADSI.](late-binding-vs--vtable-access-in-the-adsi-extension-model.md) In base al modello corrente, l'implementazione di interfacce duali non deve essere più difficile rispetto all'implementazione di interfacce dispatch.

 

 