---
title: Comunicazione client/server
description: Il meccanismo WinEvents consente ai server di comunicare facilmente con i client di Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "106299337"
---
# <a name="clientserver-communication"></a>Comunicazione client/server

Il meccanismo [winEvents](winevents-overview.md) consente ai server di comunicare facilmente con i client di Microsoft Active Accessibility. I client raccolgono spesso le informazioni rispondendo a WinEvents (ad esempio, seguendo lo stato attivo), ma sono gratuite per richiedere informazioni da un server in qualsiasi momento.

Per richiedere informazioni per un oggetto accessibile che genera un WinEvent, un client deve elaborare l'evento e stabilire una connessione con l'oggetto accessibile pertinente. A tale scopo, il client esegue i sei passaggi seguenti:

-   Un server chiama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per generare una notifica WinEvent per ogni modifica apportata agli elementi dell'interfaccia utente.
-   Il codice di gestione di WinEvent in USER determina se le applicazioni client hanno registrato una [*funzione hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e chiama la funzione di callback registrata.
-   Nella funzione di callback, il client richiede l'accesso all'oggetto che ha generato l'evento chiamando [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) o altre funzioni di recupero di oggetti accessibili. Per ulteriori informazioni, vedere [recupero di un oggetto IAccessible](retrieving-an-iaccessible-object.md).
-   Questa API Microsoft Active Accessibility invia all'applicazione server un messaggio [**WM \_ GetObject**](wm-getobject.md) per recuperare l'oggetto accessibile.
-   In risposta a [**WM \_ GetObject**](wm-getobject.md), l'applicazione server restituisce zero o restituisce un valore che funge da riferimento unico all'oggetto che ha generato l'evento.
-   Se il server restituisce zero, Microsoft Active Accessibility crea un oggetto proxy e assegna al client l'indirizzo. In caso contrario, Microsoft Active Accessibility utilizza questo riferimento per recuperare l'indirizzo di un'interfaccia oggetto, ad esempio [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o [**IDispatch**](idispatch-interface.md), e assegna tale indirizzo al client.

Una volta che il client dispone di un indirizzo di interfaccia, può chiamare le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto accessibile per recuperare le informazioni.

## <a name="in-this-section"></a>Contenuto della sezione

-   [WinEvents e Active Accessibility](winevents-overview.md)
-   [Funzionamento di WM \_ GETobject](how-wm-getobject-works.md)
-   [Recupero di un oggetto IAccessible](retrieving-an-iaccessible-object.md)

 

 




