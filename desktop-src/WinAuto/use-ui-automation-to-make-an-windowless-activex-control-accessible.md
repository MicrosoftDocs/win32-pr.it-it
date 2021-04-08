---
title: Come usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra
description: Viene descritto come usare l'automazione interfaccia utente Microsoft \ 32; API per garantire che il controllo Microsoft ActiveX senza finestra sia accessibile per le applicazioni client di Assistive Technology (AT).
ms.assetid: D584E90D-6537-4F48-8553-0DCA061FAF2A
keywords:
- Controllo ActiveX senza finestra, accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ada1d26463b0654c1808f6e4fd43f571687d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728418"
---
# <a name="how-to-use-ui-automation-to-make-a-windowless-activex-control-accessible"></a>Come usare l'automazione dell'interfaccia utente per rendere accessibile un controllo ActiveX senza finestra

Viene descritto come utilizzare l'API di automazione interfaccia utente Microsoft per assicurarsi che il controllo Microsoft ActiveX senza finestra sia accessibile per le applicazioni client di Assistive Technology (AT).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli ActiveX](/windows/desktop/com/activex-controls)
-   [Automazione interfaccia utente](entry-uiauto-win32.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione Microsoft Win32 e Component Object Model (COM)
-   Controlli ActiveX senza finestra
-   Provider di automazione interfaccia utente

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implement-the-ui-automation-provider-interfaces"></a>Passaggio 1: implementare le interfacce del provider di automazione interfaccia utente.

Per rendere accessibile l'applicazione, è necessario implementare le interfacce del provider di automazione interfaccia utente per il controllo ActiveX senza finestra, tra cui [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment), [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)e [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents). È necessario implementare queste interfacce esattamente come per un controllo basato su finestra, tranne come descritto nei passaggi seguenti. Per ulteriori informazioni sull'implementazione delle interfacce del provider UIA, vedere [UI Automation provider Programmer ' s Guide](uiauto-providerportal.md).

### <a name="step-2-implement-the-iserviceprovider-interface"></a>Passaggio 2: implementare l'interfaccia IServiceProvider.

Quando un client richiede informazioni sull'accessibilità sul controllo senza finestra, il contenitore di controlli chiama il metodo **IServiceProvider:: QueryService** del controllo per recuperare il puntatore all'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per il controllo.

Nell'esempio seguente viene illustrato come implementare il metodo **QueryService** .


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



### <a name="step-3-implement-the-irawelementproviderfragmentnavigate-method"></a>Passaggio 3: implementare il Metodo IRawElementProviderFragment:: Navigate.

Quando il metodo [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) del controllo senza finestra viene chiamato per passare al padre o a un elemento di pari livello del provider radice del controllo senza finestra, il metodo **Navigate** deve delegare al metodo [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) del contenitore di controlli.

Nell'esempio seguente viene illustrato come implementare il metodo [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) .


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



### <a name="step-4-implement-the-irawelementproviderfragmentgetruntimeid-method"></a>Passaggio 4: implementare il Metodo IRawElementProviderFragment:: GetRuntimeId.

Quando il controllo senza finestra riceve una chiamata al metodo [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid) , il controllo deve eseguire le operazioni seguenti:

1.  Recuperare un prefisso dell'ID di runtime chiamando il metodo [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sito del controllo.
2.  Creare un ID di runtime univoco per il controllo aggiungendo un intero al prefisso dell'ID di Runtime.
3.  Restituisce l'ID di runtime al chiamante.

Nell'esempio seguente viene illustrato come implementare il metodo [**GetRuntimeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) .


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

[Usare MSAA per rendere accessibile un controllo ActiveX senza finestra](use-msaa-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[Accessibilità controllo ActiveX senza finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 