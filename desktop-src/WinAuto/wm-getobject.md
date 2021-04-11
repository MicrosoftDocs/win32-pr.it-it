---
title: Messaggio WM_GETOBJECT (winuser. h)
description: Inviato da Microsoft Active Accessibility e dall'automazione interfaccia utente Microsoft per ottenere informazioni su un oggetto accessibile contenuto in un'applicazione server.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- Accessibilità Windows del messaggio WM_GETOBJECT
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121627"
---
# <a name="wm_getobject-message"></a>\_Messaggio WM GETobject

Inviato da Microsoft Active Accessibility e dall'automazione interfaccia utente Microsoft per ottenere informazioni su un oggetto accessibile contenuto in un'applicazione server.

Le applicazioni non inviano mai direttamente questo messaggio. Microsoft Active Accessibility Invia questo messaggio in risposta alle chiamate a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). Tuttavia, le applicazioni server gestiscono questo messaggio. Automazione interfaccia utente invia questo messaggio in risposta alle chiamate a [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e quando gestisce gli eventi per i quali un client ha effettuato la registrazione.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* 
</dt> <dd>

Fornisce informazioni aggiuntive sul messaggio e viene utilizzato solo dal sistema. I server passano *dwFlags* come parametro *wParam* nella chiamata a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) durante la gestione del messaggio.

</dd> <dt>

*dwObjId* 
</dt> <dd>

Identificatore di oggetto. Questo valore è una delle costanti [identificatore di oggetto](object-identifiers.md) o un identificatore di oggetto personalizzato. Un'applicazione server deve verificare questo valore per identificare il tipo di informazioni richieste. Prima di confrontare questo valore con i \_ valori ObjID, il server deve eseguire il cast a **DWORD**; in caso contrario, in Windows a 64 bit, l'estensione del segno di *lParam* può interferire con il confronto.

-   Se *dwObjId* è uno dei valori di objid \_ , ad esempio [**objid \_ client**](object-identifiers.md), la richiesta è relativa a un oggetto Active Accessibility Microsoft che implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Se *dwObjId* è uguale a **UiaRootObjectId**, la richiesta è per un provider di automazione interfaccia utente. Se il server implementa l'automazione dell'interfaccia utente, deve restituire un provider utilizzando la funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Se *dwObjId* è [**objid \_ NATIVEOM**](object-identifiers.md), la richiesta è per il modello a oggetti sottostante del controllo. Se il controllo supporta questa richiesta, deve restituire un'interfaccia COM appropriata chiamando la funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Se *dwObjId* è [**objid \_ QUERYCLASSNAMEIDX**](object-identifiers.md), la richiesta è che il controllo si identifichi come un controllo Windows standard o un controllo comune implementato dalla libreria di controlli comuni (ComCtrl.dll).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la finestra o il controllo non deve rispondere a questo messaggio, deve passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . in caso contrario, la finestra o il controllo deve restituire un valore che corrisponde alla richiesta specificata da *dwObjId*:

-   Se la finestra o il controllo implementa l'automazione dell'interfaccia utente, la finestra o il controllo deve restituire il valore ottenuto da una chiamata alla funzione [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Se *dwObjId* è [**objid \_ NATIVEOM**](object-identifiers.md) e la finestra espone un modello a oggetti nativo, Windows deve restituire il valore ottenuto da una chiamata alla funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Se *dwObjId* è [**objid \_ client**](object-identifiers.md) e la finestra implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la finestra deve restituire il valore ottenuto da una chiamata alla funzione [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

## <a name="remarks"></a>Commenti

Quando un client chiama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o qualsiasi altra funzione **AccessibleObjectFrom**_X_ che recupera un'interfaccia a un oggetto, Microsoft Active ACCESSIBILITY invia il messaggio **WM \_ GetObject** alla routine della finestra appropriata all'interno dell'applicazione server appropriata. Durante l'elaborazione di **WM \_ GetObject**, le applicazioni server chiamano [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) e usano il valore restituito di questa funzione come valore restituito per il messaggio. Microsoft Active Accessibility, in combinazione con la libreria COM, esegue il marshalling appropriato e passa di nuovo il puntatore di interfaccia dal server al client.

I server non rispondono a **WM \_ GetObject** prima che l'oggetto venga inizializzato completamente o dopo l'inizio della chiusura. Quando un'applicazione crea una nuova finestra, il sistema invia [**l' \_ oggetto evento \_ creato**](event-constants.md) per notificare ai client prima di inviare il messaggio [WM \_ create](../winmsg/wm-create.md) alla routine della finestra dell'applicazione. Poiché molte applicazioni usano WM \_ create per avviare il processo di inizializzazione, i server non rispondono al messaggio **WM \_ GetObject** fino al termine dell'elaborazione del messaggio **WM \_ create** .

Un server usa **WM \_ GetObject** per eseguire le attività seguenti:

-   [Creare nuovi oggetti accessibili](create-new-accessible-objects.md)
-   [Riutilizza puntatori esistenti a oggetti](reuse-existing-pointers-to-objects.md)
-   [Crea nuove interfacce per lo stesso oggetto](create-new-interfaces-to-the-same-object.md)

Per i client, ciò significa che potrebbero ricevere puntatori di interfaccia distinti per lo stesso elemento dell'interfaccia utente, a seconda dell'azione del server. Per determinare se due puntatori di interfaccia puntano allo stesso elemento dell'interfaccia utente, i client confrontano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto. Il confronto tra puntatori non funziona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Componente ridistribuibile<br/>          | Active Accessibility 1,3 RDK in Windows NT 4,0 con SP6 e versioni successive e Windows 95<br/>              |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Come gestire WM \_ GETobject](how-to-handle-wm-getobject.md)
</dt> <dt>

[Funzionamento di WM \_ GETobject](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

