---
title: Notifiche informative
description: Per gli Stati di connessione noti come stati in esecuzione, non è richiesta alcuna azione del gestore di notifiche a meno che non si verifichi un errore.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2020
ms.locfileid: "104472398"
---
# <a name="informational-notifications"></a>Notifiche informative

Per gli [Stati di connessione](connection-states.md) noti come stati in esecuzione, non è richiesta alcuna azione del gestore di notifiche a meno che non si verifichi un errore. Gli Stati di esecuzione si verificano durante le parti dell'operazione di connessione gestite automaticamente da RAS, ad esempio la connessione ai dispositivi necessari, l'autenticazione dell'utente e l'attesa di un callback dal server remoto. La notifica è semplicemente un report sullo stato di avanzamento per il client.

Il client può scegliere di passare le notifiche informative all'utente. In alcuni stati in esecuzione, il client potrebbe voler visualizzare informazioni aggiuntive. Ad esempio, un gestore di notifiche che riceve una \_ notifica RASCS ConnectDevice può chiamare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere il nome e il tipo del dispositivo a cui si è connessi. Un altro esempio è quando il client riceve una \_ notifica RASCS proiettata. Questo errore si verifica quando la fase di proiezione RAS dell'operazione di connessione è stata completata. Il client può chiamare la funzione [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) per ottenere informazioni aggiuntive sulla proiezione. Il client può utilizzare queste informazioni per notificare all'utente i protocolli di rete che possono essere utilizzati da questa connessione.

È consigliabile evitare di scrivere codice che dipende dall'ordine o dall'occorrenza di determinati stati informativi, perché questo può variare tra le piattaforme.

 

 




