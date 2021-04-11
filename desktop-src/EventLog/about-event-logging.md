---
description: Quando si verifica un errore, l'amministratore di sistema o il rappresentante del supporto tecnico deve determinare la causa dell'errore, tentare di recuperare i dati persi ed evitare che si verifichi un errore.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Informazioni sulla registrazione degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049599"
---
# <a name="about-event-logging"></a>Informazioni sulla registrazione degli eventi

Quando si verifica un errore, l'amministratore di sistema o il rappresentante del supporto tecnico deve determinare la causa dell'errore, tentare di recuperare i dati persi ed evitare che si verifichi un errore. È utile se le applicazioni, il sistema operativo e altri servizi di sistema registrano eventi importanti, ad esempio le condizioni di memoria insufficiente o un numero eccessivo di tentativi di accesso a un disco. L'amministratore di sistema può quindi utilizzare il registro eventi per determinare le condizioni che hanno causato l'errore e identificare il contesto in cui si è verificato. Visualizzando periodicamente il registro eventi, l'amministratore di sistema potrebbe essere in grado di identificare i problemi, ad esempio un disco rigido guasto, prima che causino danni.

> [!Note]  
> L'API di registrazione eventi è stata progettata per le applicazioni eseguite nel sistema operativo Windows Server 2003, Windows XP o Windows 2000. In Windows Vista, l'infrastruttura di registrazione degli eventi è stata riprogettata. Le applicazioni progettate per l'esecuzione nei sistemi operativi Windows Vista o versioni successive dovrebbero ora usare il [registro eventi di Windows](/windows/desktop/WES/windows-event-log) per registrare gli eventi.

 
In questa sezione viene illustrata l'interfaccia di programmazione per la scrittura e l'utilizzo di eventi mediante la registrazione degli eventi.

-   [Tipi di evento](event-types.md)
-   [Linee guida per la registrazione](logging-guidelines.md)
-   [Elementi di registrazione eventi](event-logging-elements.md)
-   [Operazioni di registrazione eventi](event-logging-operations.md)
-   [Modello di registrazione eventi](event-logging-model.md)
-   [Sicurezza registrazione eventi](event-logging-security.md)

> [!Note]  
> Le applicazioni che pubblicano eventi di dimensioni superiori a 64 kilobyte in un computer Windows Server 2003, Windows XP o Windows 2000 non saranno in grado di pubblicare eventi in un computer Windows Vista o versioni successive.
