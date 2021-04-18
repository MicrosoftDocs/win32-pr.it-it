---
title: Gestione del messaggio WM_GETOBJECT
description: Microsoft Active Accessibility e automazione interfaccia utente Microsoft inviano il \_ messaggio WM GetObject a un'applicazione server o provider per recuperare informazioni su un oggetto accessibile supportato dal server o dal provider.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695fad8f050606f0a95a1780551d35499e39d166
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300242"
---
# <a name="handling-the-wm_getobject-message"></a>Gestione del \_ messaggio WM GETobject

Microsoft Active Accessibility e automazione interfaccia utente Microsoft inviano il messaggio [**WM \_ GetObject**](wm-getobject.md) a un'applicazione server o provider per recuperare informazioni su un oggetto accessibile supportato dal server o dal provider. I client non inviano mai direttamente **WM \_ GetObject** . Al contrario, Microsoft Active Accessibility Invia questo messaggio quando un client chiama le funzioni [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)e [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . Automazione interfaccia utente **Invia WM \_ GetObject** quando un client chiama [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per i quali il client ha effettuato la registrazione.

Microsoft Active Accessibility o automazione interfaccia utente specifica il tipo di oggetto per cui è necessario ottenere informazioni passando un valore denominato *identificatore oggetto* con il messaggio [**WM \_ GetObject**](wm-getobject.md) . Quando riceve il messaggio, il server o il provider esamina l'identificatore di oggetto per determinare la modalità di risposta al messaggio. La risposta dipende dal fatto che l'applicazione ricevente implementi Microsoft Active Accessibility (un server), l'automazione interfaccia utente (un provider) o nessuna delle due per l'oggetto specificato.

-   Se l'applicazione ricevente è un server Microsoft Active Accessibility e il messaggio [**WM \_ GetObject**](wm-getobject.md) include un identificatore di oggetto del [**\_ client ObjID**](object-identifiers.md), il server deve restituire il valore ottenuto passando l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto alla funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Se l'applicazione ricevente è il provider di automazione aUI e l'identificatore di oggetto è **UiaRootObjectId**, il provider deve restituire l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) dell'oggetto. Il provider ottiene l'interfaccia chiamando la funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Se l'applicazione ricevente non implementa né Microsoft Active Accessibility né automazione interfaccia utente, deve passare il messaggio [**WM \_ GetObject**](wm-getobject.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Il passaggio del messaggio consente al Framework di accessibilità di determinare se è disponibile un proxy per l'oggetto specificato.
-   Se l'identificatore di oggetto non è né [**\_ client ObjID**](object-identifiers.md) né UiaRootObjectId, l'applicazione ricevente deve passare il messaggio [**WM \_ GetObject**](wm-getobject.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Il passaggio del messaggio consente al Framework di accessibilità di usare i provider predefiniti per gli elementi dell'interfaccia utente standard.

Microsoft Active Accessibility e automazione interfaccia utente possono passare identificatori di oggetto personalizzati in un messaggio [**WM \_ GetObject**](wm-getobject.md) per recuperare oggetti o valori definiti dall'applicazione da un server o da un provider. È possibile usare l'identificatore di oggetto [**objid \_ NATIVEOM**](object-identifiers.md) o [**objid \_ QUERYCLASSNAMEIDX**](object-identifiers.md) per recuperare un'interfaccia del modello a oggetti nativo o per richiedere un oggetto proxy specifico supportato da Oleacc.dll.

Gestendo sia gli identificatori di oggetto [**\_ client ObjID**](object-identifiers.md) che **UiaRootObjectId** , un'implementazione di Microsoft Active Accessibility server può coesistere insieme a un'implementazione del provider di automazione interfaccia utente. Poiché la maggior parte dei controlli Windows standard e dei controlli comuni implementati dalla libreria di controlli comuni (ComCtl32.dll) non implementano Microsoft Active Accessibility o l'automazione dell'interfaccia utente, questi controlli in genere non gestiscono il messaggio [**WM \_ GetObject**](wm-getobject.md) . Al contrario, il Framework di automazione interfaccia utente o Active Accessibility Microsoft verifica se è disponibile un oggetto proxy per un particolare elemento dell'interfaccia utente. In caso contrario, fornisce l'oggetto proxy predefinito per l'oggetto finestra host.

 

 