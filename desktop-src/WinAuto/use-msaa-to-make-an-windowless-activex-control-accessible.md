---
title: Usare MSAA per rendere accessibile un controllo ActiveX finestra
description: Descrive come usare l'Microsoft Active Accessibility \ 32; API per garantire che il controllo ActiveX Microsoft assistive technology sia accessibile alle applicazioni client assistive technology (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- ActiveX Controllo, accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bac5c4d2a27e5f069f2242999438eebe85e2ea7df1a6bc94890aec142db246c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098111"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Usare MSAA per rendere accessibile un controllo ActiveX finestra

Descrive come usare l'API Microsoft Active Accessibility per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile alle applicazioni client assistive technology (AT).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [ActiveX Controlli](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione Microsoft Win32 e Component Object Model (COM)
-   Controlli ActiveX finestra
-   Microsoft Active Accessibility server

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implement-the-iaccessible-interface"></a>Passaggio 1: Implementare l'interfaccia IAccessible.

Per rendere accessibile il controllo ActiveX senza finestra, è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di Microsoft Active Accessibility, esattamente come si farebbe per un controllo basato su finestra, ad eccezione di quanto descritto nei passaggi seguenti. Per altre informazioni sull'implementazione **di IAccessible,** vedere [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Passaggio 2: Implementare l'interfaccia IServiceProvider.

Quando un client richiede informazioni di accessibilità sul controllo senza finestra, il contenitore chiama il metodo [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) del controllo per recuperare il puntatore a interfaccia [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Questo esempio illustra come implementare il [**metodo QueryService.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Passaggio 3: Delegare le chiamate al metodo IAccessible::get accParent al metodo \_ IAccessibleWindowlessSite::GetParentAccessible del sito di controllo.

Quando un client richiede l'oggetto padre del controllo senza finestra, il contenitore chiama il metodo [**IAccessible::get \_ accParent del**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) controllo. **\_ L'implementazione get accParent** deve delegare al [**metodo IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenitore.

Questo esempio illustra come implementare il [**metodo \_ get accParent.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Passaggio 4: Acquisire un intervallo di ID oggetto da assegnare alle origini eventi nel controllo senza finestra.

Come i controlli basati su finestra, un controllo ActiveX finestra chiama la [**funzione NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per notificare ai client eventi importanti. I parametri della funzione includono l'ID oggetto dell'elemento che genera l'evento. Il controllo senza finestra deve assegnare gli ID oggetto usando un valore di un intervallo acquisito chiamando il metodo [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) del sito di controllo.

Questo esempio illustra come acquisire un intervallo di valori ID oggetto dal contenitore del controllo .


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Passaggio 5: Implementare l'interfaccia IAccessibleHandler.

Quando un controllo senza finestra chiama la funzione [**NotifyWinEvent,**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) il controllo specifica l'ID oggetto dell'elemento dell'interfaccia utente che genera l'evento e specifica il contenitore del controllo come finestra che risponderà ai messaggi [**WM \_ GETOBJECT**](wm-getobject.md) per conto del controllo.

Se un'applicazione client risponde all'evento , il contenitore del controllo riceve un messaggio [**WM \_ GETOBJECT**](wm-getobject.md) che include l'ID oggetto dell'elemento dell'interfaccia utente che ha generato l'evento. Il contenitore del controllo risponde cercando il controllo senza finestra che "possiede" l'ID oggetto e quindi chiamando il metodo [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) del controllo. Il **metodo AccessibleObjectFromID** restituisce il puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e il contenitore di controllo inoltra il puntatore all'applicazione client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Usare Automazione interfaccia utente per rendere accessibile un controllo ActiveX finestra](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accessibilità dei controlli ActiveX finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 