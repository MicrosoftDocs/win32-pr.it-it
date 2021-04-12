---
title: Come esporre un provider di automazione interfaccia utente Server-Side
description: Questo argomento contiene codice di esempio che illustra come esporre un provider di automazione interfaccia utente Microsoft sul lato server per un controllo personalizzato.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221640"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Come esporre un provider di automazione interfaccia utente Server-Side

Questo argomento contiene codice di esempio che illustra come esporre un provider di automazione interfaccia utente Microsoft sul lato server per un controllo personalizzato.

Automazione interfaccia utente Microsoft invia il messaggio [**WM \_ GetObject**](wm-getobject.md) a un'applicazione provider per recuperare le informazioni su un oggetto accessibile supportato dal provider. Automazione interfaccia utente **Invia WM \_ GetObject** quando un client chiama [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per i quali il client ha effettuato la registrazione.

Quando un provider riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) , deve controllare se il parametro *lParam* è uguale a **UiaRootObjectId**. In tal caso, il provider deve restituire l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) dell'oggetto. Il provider restituisce l'interfaccia chiamando la funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .

Nell'esempio seguente viene illustrato come rispondere a [**WM \_ GetObject**](wm-getobject.md).


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

[Implementazione di un provider di automazione interfaccia utente Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Messaggio WM \_ GETobject](the-wm-getobject-message.md)
</dt> <dt>

[Procedure per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




