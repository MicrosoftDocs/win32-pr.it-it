---
title: Come esporre un provider di Server-Side Automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra come esporre un provider microsoft Automazione interfaccia utente sul lato server per un controllo personalizzato.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771e81a058af16320673e46a7981cf49ee22105fa841807bc07e3a528ff223cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133314"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Come esporre un provider di Server-Side Automazione interfaccia utente

Questo argomento contiene codice di esempio che illustra come esporre un provider microsoft Automazione interfaccia utente sul lato server per un controllo personalizzato.

Microsoft Automazione interfaccia utente invia il [**messaggio WM \_ GETOBJECT**](wm-getobject.md) a un'applicazione provider per recuperare informazioni su un oggetto accessibile supportato dal provider. Automazione interfaccia utente invia **WM \_ GETOBJECT** quando un client chiama [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per cui il client ha registrato.

Quando un provider riceve un [**messaggio WM \_ GETOBJECT,**](wm-getobject.md) deve controllare se il *parametro lParam* è uguale a **UiaRootObjectId**. In caso contrario, il provider deve restituire [**l'interfaccia IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) dell'oggetto. Il provider restituisce l'interfaccia chiamando la [**funzione UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)

L'esempio seguente illustra come rispondere a [**WM \_ GETOBJECT**](wm-getobject.md).


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un provider di Server-Side Automazione interfaccia utente](uiauto-serversideprovider.md)
</dt> <dt>

[Messaggio WM \_ GETOBJECT](the-wm-getobject-message.md)
</dt> <dt>

[Procedure per i provider di Automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




