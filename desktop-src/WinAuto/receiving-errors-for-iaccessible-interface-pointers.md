---
title: Ricezione di errori per i puntatori dell'interfaccia IAccessible
description: In questo argomento vengono descritte le situazioni in cui è possibile che venga visualizzato un errore per un puntatore di interfaccia IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856546"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Ricezione di errori per i puntatori dell'interfaccia IAccessible

In questo argomento vengono descritte le situazioni in cui è possibile che venga visualizzato un errore per un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Le funzioni **IAccessible** possono restituire errori per i puntatori dell'interfaccia **IAccessible** quando un utente chiude un'applicazione a cui appartiene l'oggetto oppure se un utente chiude un controllo tramite l'interfaccia utente.

## <a name="user-closes-an-application"></a>L'utente chiude un'applicazione

Se un utente chiude l'applicazione che contiene un oggetto a cui punta il puntatore all'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , tutte le chiamate future a tale oggetto restituiranno un codice di errore. L'errore, ad esempio **Co \_ E \_ OBJNOTCONNECTED**, indicherà che l'oggetto non esiste più. Si applica a tutti i puntatori dell'interfaccia **IAccessible** .

## <a name="user-dismisses-a-control"></a>L'utente dimentica un controllo

Se un utente omette un controllo (ad esempio, premendo un pulsante di push), i client possono comunque chiamare i metodi e le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per questo oggetto perché l'oggetto non è stato rilasciato. Tuttavia, le chiamate future riceveranno messaggi di errore.

Questa situazione si applica alle funzioni e ai metodi seguenti:

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible:: Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible:: Get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




