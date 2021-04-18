---
title: Usare MSAA per rendere accessibile un controllo ActiveX senza finestra
description: Viene descritto come utilizzare Microsoft Active Accessibility \ 32; API per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile per le applicazioni client di Assistive Technology (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Controllo ActiveX, accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300182"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a>Usare MSAA per rendere accessibile un controllo ActiveX senza finestra

Viene descritto come utilizzare l'API Microsoft Active Accessibility per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile alle applicazioni client per la tecnologia assistive (AT).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione Microsoft Win32 e Component Object Model (COM)
-   Controlli ActiveX senza finestra
-   Server Microsoft Active Accessibility

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implement-the-iaccessible-interface"></a>Passaggio 1: implementare l'interfaccia IAccessible.

Per rendere accessibile il controllo ActiveX senza finestra, è necessario implementare l'interfaccia Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , come per un controllo basato su finestra, eccetto come descritto nei passaggi seguenti. Per ulteriori informazioni sull'implementazione di **IAccessible**, vedere [la guida per gli sviluppatori di Active Accessibility server](developer-s-guide-for-active-accessibility-servers.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Passaggio 2: implementare l'interfaccia IServiceProvider.

Quando un client richiede informazioni di accessibilità sul controllo senza finestra, il contenitore chiama il metodo [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) del controllo per recuperare il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Questo esempio illustra come implementare il metodo [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .


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



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a>Passaggio 3: delegare \_ le chiamate al metodo IAccessible:: get accParent al metodo IAccessibleWindowlessSite:: GetParentAccessible del sito del controllo.

Quando un client richiede l'oggetto padre del controllo senza finestra, il contenitore chiama il metodo [**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del controllo. L'implementazione di **get \_ accParent** deve delegare al metodo [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) del contenitore.

Questo esempio illustra come implementare il metodo [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .


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



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a>Passaggio 4: acquisire un intervallo di ID oggetto da assegnare alle origini eventi nel controllo privo di finestra.

Analogamente ai controlli basati su finestra, un controllo ActiveX senza finestra chiama la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per notificare ai client eventi importanti. I parametri della funzione includono l'ID oggetto dell'elemento che genera l'evento. Il controllo senza finestra deve assegnare gli ID oggetto usando un valore di un intervallo acquisito chiamando il metodo [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) del sito del controllo.

Questo esempio illustra come acquisire un intervallo di valori ID oggetto dal contenitore di controlli.


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



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a>Passaggio 5: implementare l'interfaccia IAccessibleHandler.

Quando un controllo senza finestra chiama la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , il controllo specifica l'ID oggetto dell'elemento dell'interfaccia utente che genera l'evento e specifica il contenitore di controlli come finestra che risponderà ai messaggi [**WM \_ GetObject**](wm-getobject.md) per conto del controllo.

Se un'applicazione client risponde all'evento, il contenitore di controlli riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) che include l'ID oggetto dell'elemento dell'interfaccia utente che ha generato l'evento. Il contenitore di controlli risponde cercando il controllo senza finestra che "possiede" l'ID oggetto, quindi chiamando il metodo [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) del controllo. Il metodo **AccessibleObjectFromID** restituisce il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e il contenitore di controlli lo trasmette all'applicazione client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accessibilità controllo ActiveX senza finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 