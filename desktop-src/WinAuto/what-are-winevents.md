---
title: Informazioni su WinEvent
description: Le applicazioni server e il sistema operativo usano WinEvents per notificare ai client quando si verifica una modifica nel sistema o nell'interfaccia utente.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c177183fa776a6becf52d62b86fe0ae6785c5be19dd287324ba3345b586af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563512"
---
# <a name="what-are-winevents"></a>Che cosa sono i WinEvent?

Le applicazioni server e il sistema operativo usano WinEvents per notificare ai client quando si verifica una modifica nel sistema o nell'interfaccia utente.

Il supporto di WinEvent è una funzionalità del Windows operativo che offre:

-   Un modo semplice per la registrazione dei client per le notifiche degli eventi.
-   Meccanismo per l'inserimento di codice client nei server.
-   Routing degli eventi dai server ai client interessati.
-   Generazione automatica di eventi per la maggior parte dei controlli basati su **HWND.**

La generazione di eventi per i controlli basati su **HWND** è particolarmente importante per gli sviluppatori di server. Il Microsoft Active Accessibility di esecuzione fornisce proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per tutti gli elementi standard dell'interfaccia utente. Analogamente, il sistema genera automaticamente gli eventi WinEvent appropriati ogni volta che crea, elimina, sposta, ridimensiona o esegue qualsiasi altra azione su un controllo basato su **HWND.**

Alcuni Eventi WinEvent, inclusi gli eventi **HWND** generali, sono supportati automaticamente dal sistema. Altri tipi di Eventi WinEvent, ad esempio le modifiche di stato o gli eventi di selezione specifici di un determinato controllo, sono supportati Microsoft Active Accessibility server.

Quando si verifica un evento che influisce sull'interfaccia utente, i server possono trasmettere una notifica degli eventi a tutti i client interessati chiamando la [**funzione NotifyWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) La chiamata di funzione include informazioni che identificano il tipo di evento che si è verificato e l'elemento dell'interfaccia utente a cui si applica l'evento. I client possono usare queste informazioni per recuperare un [**oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e raccogliere altre informazioni.

Ad esempio, per notificare ai client che il nome di un controllo è stato modificato, un server chiama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) e passa [**EVENT OBJECT \_ \_ NAMECHANGE**](event-constants.md) nel parametro event. Il sistema risponde determinando quali client si sono registrati per ricevere quel particolare evento e chiama la funzione di callback registrata. Se nessun client ha registrato l'evento, la chiamata del server a **NotifyWinEvent** è paragonabile a una "nessuna operazione" e l'impatto sulle prestazioni è trascurabile.

I server chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per annunciare l'evento al sistema dopo che si è verificato l'evento. Non devono mai notificare al sistema un evento prima che si verifichi l'evento.

Per ricevere notifiche sugli eventi, i client registrano le funzioni hook di callback [**usando SetWinEventHook.**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) I client impostano una singola funzione hook per tutti gli eventi possibili o più funzioni hook per intervalli discreti di eventi. Per altre informazioni, vedere [Registrazione di una funzione hook.](registering-a-hook-function.md)

Quando Microsoft Active Accessibility notifica di un evento, chiama tutte le funzioni hook registrate per tale evento, passando i parametri da [**NotifyWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)

 

 




