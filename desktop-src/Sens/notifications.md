---
description: Il servizio di notifica degli eventi di sistema consente alle applicazioni con supporto per dispositivi mobili di ricevere notifiche dagli eventi di sistema monitorati da SENS. Quando si verifica l'evento richiesto, SENS invia una notifica all'applicazione.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notifiche (Servizio notifica eventi di sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db908c48c38ccd39c6c9a427b77e3cefffc7b9bf8fad6e464ebdf146a138e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003969"
---
# <a name="notifications-system-event-notification-service"></a>Notifiche (Servizio notifica eventi di sistema)

Il servizio di notifica degli eventi di sistema consente alle applicazioni con supporto per dispositivi mobili di ricevere notifiche dagli eventi di sistema monitorati da SENS. Quando si verifica l'evento richiesto, SENS invia una notifica all'applicazione.

SENS può notificare alle applicazioni tre classi di eventi di sistema:

-   Eventi di rete TCP/IP, ad esempio lo stato di una connessione di rete TCP/IP o la qualità della connessione.
-   Eventi di accesso utente.
-   Eventi di alimentazione a batteria e CA.

Ad esempio, un'applicazione può sottoscrivere uno degli eventi di sistema seguenti:

-   Definizione della connettività di rete
-   Notifica quando una destinazione specificata può essere raggiunta entro i parametri QOC (Quality of Connection) specificati
-   Il computer è stato alimentato a batteria
-   La percentuale di potenza rimanente della batteria è all'interno di un parametro specificato
-   Si verificano eventi pianificati con Gestione sincronizzazione

**Windows Server 2008 R2 e Windows 7:** Il sottoscrittore ha un massimo di 3 minuti per rispondere a una notifica sulle interfacce [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2.**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) Dopo 3 minuti, SENS annulla la chiamata ai sottoscrittori e sblocca il thread di notifica. Se è necessaria un'operazione di lunga durata per rispondere alla notifica, restituire da **ISensLogon** o **ISensLogon2** il più rapidamente possibile e aprire un altro thread per l'elaborazione.

 

 



