---
description: Molte applicazioni registrano errori ed eventi nei log degli errori proprietari, ognuno con il proprio formato e interfaccia utente.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Registrazione eventi (registrazione eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8894c7a6d038efdc317611ca6284f62d99c82ebc767b6f96f83931803a887185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927841"
---
# <a name="event-logging-event-logging"></a>Registrazione eventi (registrazione eventi)

Molte applicazioni registrano errori ed eventi nei log degli errori proprietari, ognuno con il proprio formato e interfaccia utente. I dati di applicazioni diverse non possono essere uniti facilmente in un unico report completo, richiedendo agli amministratori di sistema o ai rappresentanti del supporto tecnico di controllare un'ampia gamma di origini per diagnosticare i problemi.

La registrazione degli eventi offre un modo centralizzato standard per le applicazioni (e il sistema operativo) di registrare importanti eventi software e hardware. Il servizio di registrazione eventi registra gli eventi provenienti da diverse origini e li archivia in un'unica raccolta denominata *log eventi*. Il Visualizzatore eventi consente di visualizzare i log. L'interfaccia di programmazione consente anche di esaminare i log.

-   [Informazioni sulla registrazione degli eventi](about-event-logging.md)
-   [Uso della registrazione eventi](using-event-logging.md)
-   [Informazioni di riferimento sulla registrazione eventi](event-logging-reference.md)

> [!Note]  
> L'API registrazione eventi è stata progettata per le applicazioni eseguite nel sistema operativo Windows Server 2003, Windows XP o Windows 2000. In Windows Vista, l'infrastruttura di registrazione degli eventi è stata riprogettata. Le applicazioni progettate per l'esecuzione Windows Vista o sistemi operativi successivi devono usare il Windows [eventi per](/windows/desktop/WES/windows-event-log) registrare gli eventi.
