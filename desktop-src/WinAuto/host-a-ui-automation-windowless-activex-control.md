---
title: Ospitare un controllo ActiveX senza finestra di automazione interfaccia utente
description: Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft ActiveX senza finestra che implementano l'automazione interfaccia utente Microsoft.
ms.assetid: A0F82968-F434-4F5E-8052-CF7CE65DB120
keywords:
- Automazione interfaccia utente, controllo ActiveX senza finestra
- Controllo ActiveX senza finestra, automazione interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77026d923ea6f0d2536cbd6a94966ec858443258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337679"
---
# <a name="host-a-ui-automation-windowless-activex-control"></a>Ospitare un controllo ActiveX senza finestra di automazione interfaccia utente

Informazioni su come creare un contenitore di controlli in grado di ospitare controlli Microsoft ActiveX senza finestra che implementano l'automazione interfaccia utente Microsoft. Utilizzando la procedura descritta in questo articolo, è possibile verificare che tutti i controlli senza finestra di automazione interfaccia utente ospitati nel contenitore di controllo siano accessibili alle applicazioni client per l'accessibilità.

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

### <a name="step-1-provide-the-irawelementprovidersimple-interface-on-behalf-of-the-windowless-control"></a>Passaggio 1: fornire l'interfaccia IRawElementProviderSimple per conto del controllo privo di finestra.

Quando il sistema richiede il puntatore [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per la radice di un controllo senza finestra, il sistema esegue una query sul contenitore di controlli. Per recuperare il puntatore, il contenitore chiama l'implementazione del controllo senza finestra del metodo [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Se il contenitore di controlli ha un'implementazione di automazione interfaccia utente, può restituire il puntatore [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) del controllo senza finestra al sistema.

Se il contenitore di controlli ha un'implementazione di Microsoft Active Accessibility, chiamare la funzione [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider) per ottenere un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) che rappresenta il controllo, quindi restituire il puntatore di interfaccia **IAccessible** al sistema.

### <a name="step-2-implement-the-irawelementproviderwindowlesssite-interface"></a>Passaggio 2: implementare l'interfaccia IRawElementProviderWindowlessSite.

Un contenitore di controlli implementa l'interfaccia [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite) Abilita un controllo senza finestra basato sull'automazione dell'interfaccia utente per comunicare le informazioni di accessibilità.

1.  Implementare [**IRawElementProviderWindowlessSite:: GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix).

    Un frammento di controllo senza finestra deve creare un ID Runtime univoco per se stesso. Per creare il relativo ID di runtime, un frammento di controllo senza finestra Recupera un valore di prefisso chiamando il metodo [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) del sito del controllo e quindi aggiunge al prefisso un valore integer univoco rispetto a tutti gli altri frammenti nel controllo senza finestra.

    Il sito di controllo per un controllo senza finestra deve implementare il metodo [**GetRuntimeIdPrefix**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix) formando un **SAFEARRAY** che contiene la costante **UiaAppendRuntimeId**, seguito da un valore integer univoco per il sito.

    Questo esempio Mostra come restituire un prefisso dell'ID di runtime per un controllo senza finestra.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
         SAFEARRAY **ppsaPrefix)   
    {   
        if (ppsaPrefix == NULL) 
        {
            return E_INVALIDARG;
        }

        // m_siteIndex is the index of the windowless control's
        // site. It is defined by the control container.
        int rId[] = { UiaAppendRuntimeId, m_siteIndex };
        SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
        if (psa == NULL)
        {
            return E_OUTOFMEMORY;
        }

        for (LONG i = 0; i < 2; i++)
        {
            SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
        }

        *ppsaPrefix = psa;  
        return S_OK;  
    }  
    ```

    

2.  Implementare il metodo [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) .

    Un controllo che implementa l'automazione dell'interfaccia utente deve restituire un puntatore al provider di frammenti padre del controllo.

    Per restituire l'elemento padre del frammento, un oggetto che implementa l'interfaccia [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) deve essere in grado di implementare il metodo [**Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) . L'implementazione di **Navigate** è difficile per un controllo senza finestra perché il controllo potrebbe non essere in grado di determinarne la posizione nell'albero accessibile dell'oggetto padre. Il metodo [**IRawElementProviderWindowlessSite:: GetAdjacentFragment**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment) consente al controllo senza finestra di eseguire una query sul relativo sito per il frammento adiacente, quindi restituisce il frammento al client che ha chiamato **Navigate**.

    Questo esempio Mostra come un contenitore di controlli Recupera il frammento padre di un controllo senza finestra.

    ```C++
    IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
            enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
    {
        if (ppFragment == NULL)
        {
            return E_INVALIDARG;
        }
        
        *ppFragment = NULL;
        HRESULT hr = S_OK;

        switch (direction)
        {
            case NavigateDirection_Parent:
                {  
                    IRawElementProviderSimple *pSimple = NULL;

                    // Call an application-defined function to retrieve the
                    // parent provider interface.
                    hr = GetParentProvider(&pSimple);  
                    if (SUCCEEDED(hr))  
                    {  
                        // Get the parent's IRawElementProviderFragment interface.
                        hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                        pSimple->Release();  
                    } 
                }  
                break;  
      
            case NavigateDirection_FirstChild:
            case NavigateDirection_LastChild:
                hr = E_INVALIDARG;
                break;

            // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
            // because there are no adjacent fragments.
            default:  
                break;  
        }  
      
        return hr;  
    }   
    ```

    

### <a name="step-3-optional-implement-the-irawelementproviderhostingaccessibles-interface"></a>Passaggio 3: facoltativo: implementare l'interfaccia IRawElementProviderHostingAccessibles.

Implementare l'interfaccia [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) se il contenitore di controlli ha un'implementazione del provider di automazione interfaccia utente che è la radice di un albero di accessibilità che include controlli ActiveX senza finestra che supportano Microsoft Active Accessibility. L'interfaccia **IRawElementProviderHostingAccessibles** ha un singolo metodo, [**GetEmbeddedAccessibles**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles), che recupera i puntatori dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di tutti i controlli ActiveX senza finestra basati su Microsoft Active Accessibility ospitati dal contenitore di controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come ospitare un controllo ActiveX senza finestra MSAA](host-an-msaa-windowless-activex-control.md)
</dt> <dt>

[Accessibilità controllo ActiveX senza finestra](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 