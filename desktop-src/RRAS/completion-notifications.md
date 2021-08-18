---
title: Notifiche di completamento
description: Il servizio di accesso Gestione connessioni continua le notifiche di stato fino al completamento dell'operazione di connessione.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6dcfad1ae0dfd4eefb3df00dceefce0df77d93239a6e7c2c4fa6517cac25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791605"
---
# <a name="completion-notifications"></a>Notifiche di completamento

Il servizio di accesso Gestione connessioni continua le notifiche di stato fino al completamento dell'operazione di connessione. Ciò si verifica nelle situazioni seguenti:

-   Il gestore riceve una notifica RASCS \_ Connected o RASCS \_ Disconnected. L'applicazione client RAS può uscire senza interrompere alcuna connessione stabilita.
-   Si verifica un errore. Il gestore riceve una notifica che indica l'errore e lo stato della connessione quando si è verificato l'errore. L'applicazione client RAS può essere chiusa.

L'applicazione client RAS non deve presupporre che l'operazione di connessione sia stata completata dopo [**la chiamata di RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa). Deve attendere una delle condizioni precedenti prima di uscire.

 

 




