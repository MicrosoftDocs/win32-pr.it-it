---
title: Notifiche di completamento
description: La gestione connessione di accesso remoto continua le notifiche di stato fino al completamento dell'operazione di connessione.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044755"
---
# <a name="completion-notifications"></a>Notifiche di completamento

La gestione connessione di accesso remoto continua le notifiche di stato fino al completamento dell'operazione di connessione. Questo problema si verifica nelle situazioni seguenti:

-   Il gestore riceve una \_ notifica RASCS connessa o RASCS \_ disconnessa. L'applicazione client RAS può uscire senza interruzioni della connessione stabilita.
-   Si è verificato un errore. Il gestore riceve una notifica che indica l'errore e lo stato della connessione quando si è verificato l'errore. È possibile uscire dall'applicazione client RAS.

L'applicazione client RAS non deve presupporre che l'operazione di connessione venga completata dopo la chiamata a [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa). Deve attendere una delle condizioni precedenti prima di uscire.

 

 




