---
title: Come usare Automazione interfaccia utente rendere accessibile un controllo ActiveX finestra
description: Descrive come usare Microsoft Automazione interfaccia utente \ 32; API per garantire che il controllo ActiveX Microsoft assistive technology sia accessibile alle applicazioni client assistive technology (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Controllo ActiveX finestra, accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ef56d5f3a06bbfa21502c791163f2251506a10fda7da9d07ee04941ad39de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570361"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>Come usare Automazione interfaccia utente rendere accessibile un controllo ActiveX finestra

Descrive come usare l'API Microsoft Automazione interfaccia utente per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile alle applicazioni client assistive technology (AT).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [ActiveX Controlli](/windows/desktop/com/activex-controls)
-   [Automazione interfaccia utente](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione Microsoft Win32 e Component Object Model (COM)
-   Controlli ActiveX finestra
-   Automazione interfaccia utente provider

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Passaggio 1: Implementare le interfacce Automazione interfaccia utente provider.

Per rendere accessibile l'applicazione, è necessario implementare le interfacce del provider Automazione interfaccia utente per il controllo ActiveX senza finestra, tra cui [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)e [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). È consigliabile implementare queste interfacce esattamente come si farebbe per un controllo basato su finestra, tranne come descritto nei passaggi seguenti. Per altre informazioni sull'implementazione delle interfacce del provider UIA, vedere [Automazione interfaccia utente Provider Programmer's Guide](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Passaggio 2: Implementare l'interfaccia IServiceProvider.

Quando un client necessita di informazioni di accessibilità sul controllo senza finestra, il contenitore del controllo chiama il metodo **IServiceProvider::QueryService** del controllo per recuperare il puntatore a interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per il controllo.

Nell'esempio seguente viene illustrato come implementare il **metodo QueryService.**


```C++
STDMETHODIMP CMyAccessibleUIAControl::QueryService(REFGUID guidService,
        REFIID riid, void **ppvObject)
{  
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL; 
 
    if (guidService == __uuidof(IRawElementProviderSimple))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Passaggio 3: Implementare il metodo IRawElementProviderFragment::Navigate.

Quando viene chiamato il metodo [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) del controllo senza finestra per passare all'elemento padre o a un elemento di pari livello del provider radice del controllo senza finestra, il metodo **Navigate** deve delegare al metodo [**IRawElementProviderWindowlessSite::GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) del contenitore di controlli.

Nell'esempio seguente viene illustrato come implementare il [**metodo Navigate.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)


```C++
STDMETHODIMP CMyAccessibleUIAControl::Navigate(NavigateDirection direction,
     IRawElementProviderFragment **ppRetVal) 
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  
    
    if (direction == NavigateDirection_Parent)  
    {  
        // Query the control container's windowless site 
        // for the parent.
         if (SUCCEEDED(m_pClientSite->QueryInterface(
                IID_PPV_ARGS(&pWindowlessSite))))  
        {  
            hr =  pWindowlessSite->GetAdjacentFragment(direction, ppRetVal);  
        }  
    }  

    else if (direction == NavigateDirection_FirstChild)  
    {  
        // GetFragmentForChild is an application-defined function that 
        // retrieves the first or last child fragment.
        hr =  GetFragmentForChild(FIRST, ppRetVal);  
    }  

    else if (direction == NavigateDirection_LastChild)  
    {  
        hr = GetFragmentForChild(LAST, ppRetVal);  
    }  

    SafeRelease(&pWindowlessSite);
    return S_OK;   
}
```



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Passaggio 4: Implementare il metodo IRawElementProviderFragment::GetRuntimeId.

Quando il controllo senza finestra riceve una chiamata al relativo metodo [**IRawElementProviderFragment::GetRuntimeId,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) il controllo deve eseguire le operazioni seguenti:

1.  Recuperare un prefisso ID di runtime chiamando il metodo [**IRawElementProviderWindowlessSite::GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sito di controllo.
2.  Creare un ID di runtime univoco per il controllo aggiungendo un numero intero al prefisso DELL'ID di runtime.
3.  Restituire l'ID di runtime al chiamante.

L'esempio seguente illustra come implementare il [**metodo GetRuntimeId.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix)


```C++
STDMETHODIMP CMyAccessibleUIAControl::GetRuntimeId(SAFEARRAY **ppRetVal)  
{   
    if (ppRetVal == NULL)
    {
        return E_INVALIDARG;
    }

    *ppRetVal = NULL;  
    HRESULT hr = E_FAIL;
    IRawElementProviderWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        // Create a safe array to hold runtime ID.
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 1, 3);  
        if (psa == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Retrieve the runtime ID prefix from the control container. The prefix
        // consists of UiaAppendRuntimeId followed by the windowless site ID.
        if (SUCCEEDED(hr))
        {    
            hr = pWindowlessSite->GetRuntimeIdPrefix(&psa);  
        } 

        if (SUCCEEDED(hr))
        {
        // Append this fragment's ID to the retrieved runtime ID prefix.
            long i = 2;
            hr = SafeArrayPutElement(psa, &i, (void*)&m_Id);        
        }

        if (SUCCEEDED(hr))
        {
            *ppRetVal = psa;  
        }
    }

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Usare MSAA per rendere accessibile un controllo ActiveX finestra](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accessibilità dei controlli ActiveX finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 