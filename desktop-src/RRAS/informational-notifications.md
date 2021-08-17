---
title: Notifiche in tempo reale
description: Per gli stati di connessione noti come stati di esecuzione, non è necessaria alcuna azione del gestore di notifica a meno che non si verifichi un errore.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f526dcd0cd52eaa15929f970debe3ba78788fdb7525e734ee2e26e348b32552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790995"
---
# <a name="informational-notifications"></a>Notifiche in tempo reale

Per gli [stati di connessione](connection-states.md) noti come stati di esecuzione, non è necessaria alcuna azione del gestore di notifica a meno che non si verifichi un errore. Gli stati di esecuzione si verificano durante le parti dell'operazione di connessione che RAS gestisce automaticamente, ad esempio la connessione ai dispositivi necessari, l'autenticazione dell'utente e l'attesa di un callback dal server remoto. La notifica è semplicemente un report di stato per il client.

Il client può scegliere di passare queste notifiche in informazioni all'utente. In alcuni stati di esecuzione, il client potrebbe voler visualizzare informazioni aggiuntive. Ad esempio, un gestore di notifica che riceve una notifica RasCS ConnectDevice può chiamare la \_ [**funzione RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere il nome e il tipo del dispositivo a cui si è connessi. Un altro esempio è quando il client riceve una notifica \_ proiettata RASCS. Ciò si verifica quando la fase di proiezione RAS dell'operazione di connessione è stata completata. Il client può chiamare la [**funzione RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) per ottenere informazioni aggiuntive sulla proiezione. Il client può utilizzare queste informazioni per notificare all'utente quali protocolli di rete possono essere utilizzati da questa connessione.

È consigliabile evitare di scrivere codice che dipende dall'ordine o dall'occorrenza di determinati stati in informazioni, perché ciò può variare tra le piattaforme.

 

 




