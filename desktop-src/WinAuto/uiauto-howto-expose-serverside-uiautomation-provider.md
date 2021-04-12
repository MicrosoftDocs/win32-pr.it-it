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
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="67c56-103">Come esporre un provider di automazione interfaccia utente Server-Side</span><span class="sxs-lookup"><span data-stu-id="67c56-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="67c56-104">Questo argomento contiene codice di esempio che illustra come esporre un provider di automazione interfaccia utente Microsoft sul lato server per un controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="67c56-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="67c56-105">Automazione interfaccia utente Microsoft invia il messaggio [**WM \_ GetObject**](wm-getobject.md) a un'applicazione provider per recuperare le informazioni su un oggetto accessibile supportato dal provider.</span><span class="sxs-lookup"><span data-stu-id="67c56-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="67c56-106">Automazione interfaccia utente **Invia WM \_ GetObject** quando un client chiama [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per i quali il client ha effettuato la registrazione.</span><span class="sxs-lookup"><span data-stu-id="67c56-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="67c56-107">Quando un provider riceve un messaggio [**WM \_ GetObject**](wm-getobject.md) , deve controllare se il parametro *lParam* è uguale a **UiaRootObjectId**.</span><span class="sxs-lookup"><span data-stu-id="67c56-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="67c56-108">In tal caso, il provider deve restituire l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="67c56-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="67c56-109">Il provider restituisce l'interfaccia chiamando la funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="67c56-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="67c56-110">Nell'esempio seguente viene illustrato come rispondere a [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="67c56-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="67c56-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67c56-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67c56-112">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="67c56-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67c56-113">Implementazione di un provider di automazione interfaccia utente Server-Side</span><span class="sxs-lookup"><span data-stu-id="67c56-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="67c56-114">Messaggio WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="67c56-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="67c56-115">Procedure per i provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="67c56-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




