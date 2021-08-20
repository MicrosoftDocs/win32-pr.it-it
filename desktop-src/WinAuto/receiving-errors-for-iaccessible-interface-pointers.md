---
title: Ricezione di errori per puntatori a interfaccia IAccessible
description: In questo argomento vengono descritte le situazioni in cui potrebbe essere visualizzato un errore per un puntatore a interfaccia IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d36a29c688966526d5431e1fe2f643e39b378779d122d22f38dea2089a5191c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115142"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Ricezione di errori per puntatori a interfaccia IAccessible

In questo argomento vengono descritte le situazioni in cui potrebbe essere visualizzato un errore per un [**puntatore a interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) **Le funzioni IAccessible** possono restituire errori per i puntatori a interfaccia **IAccessible** quando un utente chiude un'applicazione a cui appartiene l'oggetto o se un utente chiude un controllo tramite l'interfaccia utente.

## <a name="user-closes-an-application"></a>L'utente chiude un'applicazione

Se un utente chiude l'applicazione che contiene un oggetto a cui puntava il puntatore di interfaccia [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) tutte le chiamate future a tale oggetto restituiranno un codice di errore. L'errore, ad **esempio CO \_ E \_ OBJNOTCONNECTED,** indicherà che l'oggetto non esiste più. Questo vale per tutti i puntatori a interfaccia **IAccessible.**

## <a name="user-dismisses-a-control"></a>L'utente ignora un controllo

Se un utente chiude un controllo ,ad esempio premendo un pulsante di comando, i client possono comunque chiamare i metodi e le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) su questo oggetto perché l'oggetto non è stato rilasciato. Tuttavia, le chiamate future riceveranno messaggi di errore.

Questa situazione si applica alle funzioni e ai metodi seguenti:

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible::get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible::get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




