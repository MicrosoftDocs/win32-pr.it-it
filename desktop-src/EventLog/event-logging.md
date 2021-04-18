---
description: Molte applicazioni registrano gli errori e gli eventi nei log degli errori proprietari, ognuno con il proprio formato e l'interfaccia utente.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Registrazione eventi (registrazione eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316790"
---
# <a name="event-logging-event-logging"></a>Registrazione eventi (registrazione eventi)

Molte applicazioni registrano gli errori e gli eventi nei log degli errori proprietari, ognuno con il proprio formato e l'interfaccia utente. Non è possibile unire facilmente i dati di applicazioni diverse in un unico report completo, in modo da richiedere agli amministratori di sistema o ai rappresentanti del supporto tecnico di controllare un'ampia gamma di origini per diagnosticare i problemi.

La registrazione degli eventi fornisce un metodo standard e centralizzato per le applicazioni (e il sistema operativo) per la registrazione di importanti eventi software e hardware. Il servizio di registrazione eventi registra gli eventi da diverse origini e li archivia in una singola raccolta denominata *log eventi*. Il Visualizzatore eventi consente di visualizzare i log. l'interfaccia di programmazione consente inoltre di esaminare i log.

-   [Informazioni sulla registrazione degli eventi](about-event-logging.md)
-   [Uso della registrazione eventi](using-event-logging.md)
-   [Riferimento per la registrazione eventi](event-logging-reference.md)

> [!Note]  
> L'API di registrazione eventi è stata progettata per le applicazioni eseguite nel sistema operativo Windows Server 2003, Windows XP o Windows 2000. In Windows Vista, l'infrastruttura di registrazione degli eventi è stata riprogettata. Le applicazioni progettate per l'esecuzione in Windows Vista o sistemi operativi successivi devono usare il [registro eventi di Windows](/windows/desktop/WES/windows-event-log) per registrare gli eventi.
