---
title: Che cosa sono WinEvents
description: Le applicazioni server e il sistema operativo utilizzano WinEvents per notificare ai client quando si verifica una modifica nel sistema o nell'interfaccia utente.
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97864f2b1464718680d781ad843345f1e46fce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298753"
---
# <a name="what-are-winevents"></a>Che cosa sono WinEvents?

Le applicazioni server e il sistema operativo utilizzano WinEvents per notificare ai client quando si verifica una modifica nel sistema o nell'interfaccia utente.

Il supporto di WinEvent è una funzionalità del sistema operativo Windows che fornisce:

-   Un modo semplice per i client di registrarsi per le notifiche degli eventi.
-   Meccanismo per inserire il codice client nei server.
-   Routing degli eventi dai server ai client interessati.
-   Generazione automatica di eventi per la maggior parte dei controlli basati su **HWND**.

La generazione di eventi per i controlli basati su **HWND** è particolarmente importante per gli sviluppatori di server. La fase di esecuzione di Microsoft Active Accessibility fornisce proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per tutti gli elementi dell'interfaccia utente standard. Analogamente, il sistema genera automaticamente il WinEvents appropriato ogni volta che crea, Elimina, sposta, ridimensiona o esegue altre azioni su un controllo basato su **HWND**.

Alcuni WinEvents, inclusi gli eventi **HWND** generali, sono supportati automaticamente dal sistema. Altri tipi di WinEvents, ad esempio modifiche di stato o eventi di selezione specifici di un determinato controllo, sono supportati dai server Microsoft Active Accessibility.

Quando si verifica un evento che influisca sull'interfaccia utente, i server possono trasmettere una notifica degli eventi a tutti i client interessati chiamando la funzione [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) . La chiamata di funzione include informazioni che identificano il tipo di evento che si è verificato e l'elemento dell'interfaccia utente a cui si applica l'evento. I client possono utilizzare queste informazioni per recuperare un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento dell'interfaccia utente e raccogliere ulteriori informazioni.

Ad esempio, per notificare ai client che il nome di un controllo è stato modificato, un server chiama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) e passa l' [**\_ oggetto evento \_ NAMECHANGE**](event-constants.md) nel parametro dell'evento. Il sistema risponde determinando quali client hanno registrato per ricevere l'evento specifico e chiama la funzione di callback registrata. Se non è stato registrato alcun client per l'evento, la chiamata del server a **NotifyWinEvent** è paragonabile a un'operazione "No" e l'effetto sulle prestazioni è irrilevante.

I server chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per annunciare l'evento al sistema dopo che si è verificato l'evento. Non devono mai inviare notifiche al sistema di un evento prima che si verifichi l'evento.

Per ricevere notifiche relative agli eventi, i client registrano funzioni hook di callback usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). I client impostano una singola funzione hook per tutti i possibili eventi o più funzioni hook per intervalli discreti di eventi. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di una funzione hook](registering-a-hook-function.md).

Quando Microsoft Active Accessibility riceve una notifica di un evento, chiama tutte le funzioni hook registrate per tale evento, passando i parametri da [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).

 

 




