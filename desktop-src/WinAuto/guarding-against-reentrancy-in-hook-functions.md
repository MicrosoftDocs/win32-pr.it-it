---
title: Protezione dalla reentrancy nelle funzioni hook
description: Durante l'elaborazione di un evento da parte di una funzione hook, è possibile che siano attivati eventi aggiuntivi, che potrebbero causare il reenter della funzione hook prima del termine dell'elaborazione dell'evento originale.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089ac7212823bc64d6c59cdae3d333e96760dfbc25c899cea80071bb39799c17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030751"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Protezione dalla reentrancy nelle funzioni hook

Durante l'elaborazione di un evento da parte di una funzione hook, è possibile che siano attivati eventi aggiuntivi, che potrebbero causare il reenter della funzione hook prima del termine dell'elaborazione dell'evento originale. Il problema della reentrancy nelle funzioni hook è che gli eventi vengono completati fuori sequenza a meno che la funzione hook non gestisca questa situazione.

Si consideri ad esempio un caso in cui una funzione hook in un programma di lettura dello schermo sta elaborando [**l'evento EVENT \_ OBJECT \_ VALUECHANGE**](event-constants.md) per un controllo di modifica. Se, durante l'elaborazione del primo evento di modifica del valore, la funzione hook rientra per elaborare un evento di modifica del valore successivo, il secondo evento viene completato prima del primo evento. Questa situazione comporta che l'utilità per la lettura dello schermo trasla informazioni non accurate all'utente.

Poiché l'elaborazione degli eventi viene interrotta, è possibile ricevere eventi aggiuntivi ogni volta che la funzione hook chiama una funzione che determina il controllo della coda di messaggi del thread proprietario. Ciò si verifica quando una delle operazioni seguenti viene chiamata all'interno della funzione hook:

-   Funzione Windows [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) [**GetMessage,**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage,**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) [**o MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   Le Microsoft Active Accessibility funzioni [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**Un'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o un Component Object Model (COM) o un altro metodo che attraversa i limiti del processo

Poiché le funzioni hook chiamano le proprietà e i metodi [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) e [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) non è possibile impedire la reentrancy. L'unica soluzione è che gli sviluppatori client possano aggiungere codice nella funzione hook che rileva la reentrancy e intraprendere le azioni appropriate se la funzione hook viene rientrata.

 

 