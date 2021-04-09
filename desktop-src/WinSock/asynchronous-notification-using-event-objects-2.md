---
description: Le funzioni WSAEventSelect e WSAEnumNetworkEvents vengono fornite per supportare applicazioni quali daemon e servizi senza interfaccia utente (e di conseguenza non utilizzano handle di Windows).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Notifica asincrona mediante oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879234"
---
# <a name="asynchronous-notification-using-event-objects"></a>Notifica asincrona mediante oggetti evento

Le funzioni [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) e [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) vengono fornite per supportare applicazioni quali daemon e servizi senza interfaccia utente (e di conseguenza non utilizzano handle di Windows). La funzione **WSAEventSelect** si comporta esattamente come la funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Tuttavia, anziché fare in modo che un messaggio di Windows venga inviato quando si verifica un \_ evento di rete FD xxx (ad esempio, \_ lettura FD e \_ scrittura FD), viene impostato un oggetto evento designato dall'applicazione.

Inoltre, il fatto che si \_ sia verificato un evento di rete FD XXX specifico viene memorizzato dal provider di servizi. L'applicazione può chiamare [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) per fare in modo che il contenuto corrente della memoria degli eventi di rete venga copiato in un buffer fornito dall'applicazione e che la memoria dell'evento di rete venga cancellata automaticamente. Se necessario, l'applicazione può anche designare un particolare oggetto evento che viene cancellato insieme alla memoria dell'evento di rete.

 

 



