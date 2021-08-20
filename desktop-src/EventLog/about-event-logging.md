---
description: Quando si verifica un errore, l'amministratore di sistema o il rappresentante del supporto deve determinare la causa dell'errore, tentare di recuperare i dati persi ed evitare che l'errore si ripeta.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Informazioni sulla registrazione degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9f30e4f8a44594b95215d748ac5cafda6b0633eefa668d0d864362c8f3c5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814258"
---
# <a name="about-event-logging"></a>Informazioni sulla registrazione degli eventi

Quando si verifica un errore, l'amministratore di sistema o il rappresentante del supporto deve determinare la causa dell'errore, tentare di recuperare i dati persi ed evitare che l'errore si ripeta. È utile se le applicazioni, il sistema operativo e altri servizi di sistema registrano eventi importanti, ad esempio condizioni di memoria insufficiente o tentativi eccessivi di accedere a un disco. L'amministratore di sistema può quindi usare il registro eventi per determinare quali condizioni hanno causato l'errore e identificare il contesto in cui si è verificato. Visualizzando periodicamente il registro eventi, l'amministratore di sistema potrebbe essere in grado di identificare i problemi (ad esempio un disco rigido in errore) prima che si verificano danni.

> [!Note]  
> L'API Registrazione eventi è stata progettata per le applicazioni eseguite nel sistema operativo Windows Server 2003, Windows XP o Windows 2000. In Windows Vista, l'infrastruttura di registrazione eventi è stata riprogettata. Le applicazioni progettate per l'esecuzione nei sistemi operativi Windows Vista o versioni successive devono ora usare Windows [eventi](/windows/desktop/WES/windows-event-log) per registrare gli eventi.

 
In questa sezione viene illustrata l'interfaccia di programmazione per la scrittura e l'utilizzo di eventi tramite la registrazione eventi.

-   [Tipi di evento](event-types.md)
-   [Linee guida per la registrazione](logging-guidelines.md)
-   [Elementi di registrazione eventi](event-logging-elements.md)
-   [Operazioni di registrazione eventi](event-logging-operations.md)
-   [Modello di registrazione eventi](event-logging-model.md)
-   [Sicurezza della registrazione eventi](event-logging-security.md)

> [!Note]  
> Le applicazioni che pubblicano eventi di dimensioni superiori a 64 kilobyte in un computer Windows Server 2003, Windows XP o Windows 2000 non saranno in grado di pubblicare eventi in un computer Windows Vista o versioni successive.
