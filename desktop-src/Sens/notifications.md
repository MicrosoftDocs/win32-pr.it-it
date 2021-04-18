---
description: Il servizio di notifica eventi di sistema consente alle applicazioni compatibili con dispositivi mobili di ricevere notifiche dagli eventi di sistema monitorati da SENS. Quando si verifica l'evento richiesto, SENS invia una notifica all'applicazione.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notifiche (servizio di notifica eventi di sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316628"
---
# <a name="notifications-system-event-notification-service"></a>Notifiche (servizio di notifica eventi di sistema)

Il servizio di notifica eventi di sistema consente alle applicazioni compatibili con dispositivi mobili di ricevere notifiche dagli eventi di sistema monitorati da SENS. Quando si verifica l'evento richiesto, SENS invia una notifica all'applicazione.

SENS può notificare alle applicazioni circa tre classi di eventi di sistema:

-   Eventi di rete TCP/IP, ad esempio lo stato di una connessione di rete TCP/IP o la qualità della connessione.
-   Eventi di accesso utente.
-   Eventi di alimentazione a batteria e AC.

Ad esempio, un'applicazione può sottoscrivere uno qualsiasi degli eventi di sistema seguenti:

-   Creazione della connettività di rete
-   Notifica quando è possibile raggiungere una destinazione specificata entro i parametri di qualità della connessione (QOC) specificati
-   Il computer è stato alimentato a batteria
-   La percentuale di alimentazione della batteria rimanente rientra in un parametro specificato
-   Eventi pianificati con Gestione sincronizzazione

**Windows Server 2008 R2 e Windows 7:** Il Sottoscrittore è costituito da un massimo di 3 minuti per rispondere a una notifica sulle interfacce [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) . Dopo 3 minuti, SENS Annulla la chiamata ai sottoscrittori e sblocca il thread di notifica. Se è necessaria un'operazione di lunga durata per rispondere alla notifica, restituire da **ISensLogon** o **ISensLogon2** il più rapidamente possibile e aprire un altro thread per l'elaborazione.

 

 



