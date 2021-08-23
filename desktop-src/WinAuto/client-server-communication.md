---
title: Comunicazione client/server
description: Il meccanismo WinEvents consente ai server di comunicare facilmente con Microsoft Active Accessibility client.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896b6f6688e0e2929ebb351fe9d7cc210803768a8031faa44a8aca8127b12002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133934"
---
# <a name="clientserver-communication"></a>Comunicazione client/server

Il [meccanismo WinEvents](winevents-overview.md) consente ai server di comunicare facilmente con Microsoft Active Accessibility client. I client spesso raccolgono informazioni rispondendo a WinEvent (ad esempio, seguendo lo stato attivo), ma sono liberi di richiedere informazioni da un server in qualsiasi momento.

Per richiedere informazioni per un oggetto accessibile che genera un WinEvent, un client deve elaborare l'evento e stabilire una connessione con l'oggetto accessibile pertinente. A tale scopo, il client esegue i sei passaggi seguenti:

-   Un server chiama [**NotifyWinEvent per**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) generare una notifica WinEvent per ogni modifica agli elementi dell'interfaccia utente.
-   Il codice di gestione WinEvent in USER determina se le applicazioni client hanno registrato una funzione [*hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent [**usando SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e chiama la funzione di callback registrata.
-   Nella funzione di callback il client richiede l'accesso all'oggetto che ha generato l'evento chiamando [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) o altre funzioni di recupero di oggetti accessibili. Per altre informazioni, vedere [Recupero di un oggetto IAccessible.](retrieving-an-iaccessible-object.md)
-   Questa API Microsoft Active Accessibility invia all'applicazione server un [**messaggio WM \_ GETOBJECT**](wm-getobject.md) per recuperare l'oggetto accessibile.
-   In risposta a [**WM \_ GETOBJECT,**](wm-getobject.md)l'applicazione server restituisce zero o un valore che funge da riferimento una sola volta all'oggetto che ha generato l'evento.
-   Se il server restituisce zero, Microsoft Active Accessibility crea un oggetto proxy e assegna il relativo indirizzo al client. In caso Microsoft Active Accessibility usa questo riferimento per recuperare l'indirizzo di un'interfaccia oggetto, ad esempio [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o [**IDispatch,**](idispatch-interface.md)e fornisce tale indirizzo al client.

Quando il client ha un indirizzo di interfaccia, può chiamare le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto accessibile per recuperare le informazioni.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Eventi WinEvent e Active Accessibility](winevents-overview.md)
-   [Funzionamento di WM \_ GETOBJECT](how-wm-getobject-works.md)
-   [Recupero di un oggetto IAccessible](retrieving-an-iaccessible-object.md)

 

 




