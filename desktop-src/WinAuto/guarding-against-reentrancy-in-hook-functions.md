---
title: Protezione contro la rientranza nelle funzioni hook
description: Mentre una funzione hook elabora un evento, è possibile che vengano generati eventi aggiuntivi, che potrebbero causare la reimmissione della funzione hook prima del completamento dell'elaborazione dell'evento originale.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399485"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Protezione contro la rientranza nelle funzioni hook

Mentre una funzione hook elabora un evento, è possibile che vengano generati eventi aggiuntivi, che potrebbero causare la reimmissione della funzione hook prima del completamento dell'elaborazione dell'evento originale. Il problema con la rientranza nelle funzioni hook è che gli eventi vengono completati fuori sequenza, a meno che la funzione hook non gestisca questa situazione.

Si consideri, ad esempio, un caso in cui una funzione hook in un programma di lettura schermo sta elaborando l'evento [**\_ \_ VALUECHANGE dell'oggetto evento**](event-constants.md) per un controllo di modifica. Se, durante l'elaborazione dell'evento di modifica del primo valore, la funzione hook viene nuovamente immessa per elaborare un evento di modifica del valore successivo, il secondo evento viene completato prima del primo evento. Questa situazione restituisce all'utente informazioni non accurate da parte dell'utente.

Poiché l'elaborazione degli eventi viene interrotta, è possibile che vengano ricevuti eventi aggiuntivi ogni volta che la funzione hook chiama una funzione che determina il controllo della coda di messaggi del thread proprietario. Questo errore si verifica quando una qualsiasi delle operazioni seguenti viene chiamata all'interno della funzione hook:

-   Funzione Windows [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage), [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea), [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)o [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   Funzioni di Microsoft Active Accessibility [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o altra proprietà o metodo di Component Object Model (com) che supera i limiti del processo

Poiché le funzioni hook chiamano proprietà e metodi [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) e [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , non è possibile impedire la rientranza. L'unica soluzione consiste nel consentire agli sviluppatori di client di aggiungere codice nella funzione hook che rilevi la rientranza e intraprendere le azioni appropriate se la funzione hook viene nuovamente immessa.

 

 