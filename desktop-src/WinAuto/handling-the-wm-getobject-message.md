---
title: Gestione del messaggio WM_GETOBJECT
description: Sia Microsoft Active Accessibility che Microsoft Automazione interfaccia utente inviare il messaggio WM GETOBJECT a un'applicazione server o provider per recuperare informazioni su un oggetto accessibile supportato dal server o \_ dal provider.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732ebd21cc6d198040e5502554ce2a8cf1abb718c055bc9af9f88e0c5d123b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994191"
---
# <a name="handling-the-wm_getobject-message"></a>Gestione del messaggio WM \_ GETOBJECT

Sia Microsoft Active Accessibility che Microsoft Automazione interfaccia utente inviare il messaggio [**WM \_ GETOBJECT**](wm-getobject.md) a un'applicazione server o provider per recuperare informazioni su un oggetto accessibile supportato dal server o dal provider. I client non **inviano mai direttamente WM \_ GETOBJECT.** Al contrario, Microsoft Active Accessibility questo messaggio quando un client chiama le funzioni [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)e [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Automazione interfaccia utente invia **WM \_ GETOBJECT** quando un client chiama [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per cui il client ha registrato.

Microsoft Active Accessibility o Automazione interfaccia utente il tipo di oggetto per cui sono necessarie informazioni passando un valore denominato identificatore di oggetto *con* il messaggio [**WM \_ GETOBJECT.**](wm-getobject.md) Quando riceve il messaggio, il server o il provider esamina l'identificatore di oggetto per determinare come rispondere al messaggio. La risposta dipende dal fatto che l'applicazione ricevente implementi Microsoft Active Accessibility (un server), Automazione interfaccia utente (un provider) o nessuno dei due per l'oggetto specificato.

-   Se l'applicazione ricevente è un server Microsoft Active Accessibility e il messaggio [**WM \_ GETOBJECT**](wm-getobject.md) include un identificatore di oggetto [**OBJID \_ CLIENT,**](object-identifiers.md)il server deve restituire il valore ottenuto passando l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto alla funzione [**LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Se l'applicazione ricevente è un provider di automazione interfaccia utente e l'identificatore di oggetto è **UiaRootObjectId,** il provider deve restituire [**l'interfaccia IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) dell'oggetto. Il provider ottiene l'interfaccia chiamando la [**funzione UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
-   Se l'applicazione ricevente non implementa né Microsoft Active Accessibility né Automazione interfaccia utente, deve passare il messaggio [**WM \_ GETOBJECT**](wm-getobject.md) alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Il passaggio del messaggio consente al framework di accessibilità di determinare se è disponibile un proxy per l'oggetto specificato.
-   Se l'identificatore di oggetto non è [**NÉ OBJID \_ CLIENT**](object-identifiers.md) né UiaRootObjectId, l'applicazione ricevente deve passare il messaggio [**WM \_ GETOBJECT**](wm-getobject.md) alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Il passaggio del messaggio consente al framework di accessibilità di usare i provider predefiniti per gli elementi dell'interfaccia utente standard.

Microsoft Active Accessibility e Automazione interfaccia utente gli identificatori di oggetto personalizzati in un messaggio [**WM \_ GETOBJECT**](wm-getobject.md) per recuperare valori o oggetti definiti dall'applicazione da un server o da un provider. L'identificatore di oggetto [**OBJID \_ NATIVEOM**](object-identifiers.md) o [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) può essere usato per recuperare un'interfaccia nativa del modello a oggetti o per richiedere un oggetto proxy specifico supportato da Oleacc.dll.

Gestendo gli identificatori di oggetto [**OBJID \_ CLIENT**](object-identifiers.md) e **UiaRootObjectId,** un'implementazione del server Microsoft Active Accessibility può coesistere insieme a un'implementazione Automazione interfaccia utente provider di dati. Poiché la maggior parte dei controlli Windows standard e i controlli comuni implementati dalla libreria di controlli comuni (ComCtl32.dll) non implementano Microsoft Active Accessibility o Automazione interfaccia utente, questi controlli in genere non gestiscono il messaggio [**WM \_ GETOBJECT.**](wm-getobject.md) Al contrario, il Microsoft Active Accessibility o Framework di automazione interfaccia utente verifica se un oggetto proxy è disponibile per un particolare elemento dell'interfaccia utente. In caso contrario, fornisce l'oggetto proxy predefinito per l'oggetto finestra host.

 

 