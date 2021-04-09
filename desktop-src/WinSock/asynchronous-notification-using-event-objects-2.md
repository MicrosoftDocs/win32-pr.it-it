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
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="f5059-103">Notifica asincrona mediante oggetti evento</span><span class="sxs-lookup"><span data-stu-id="f5059-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="f5059-104">Le funzioni [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) e [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) vengono fornite per supportare applicazioni quali daemon e servizi senza interfaccia utente (e di conseguenza non utilizzano handle di Windows).</span><span class="sxs-lookup"><span data-stu-id="f5059-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="f5059-105">La funzione **WSAEventSelect** si comporta esattamente come la funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) .</span><span class="sxs-lookup"><span data-stu-id="f5059-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="f5059-106">Tuttavia, anziché fare in modo che un messaggio di Windows venga inviato quando si verifica un \_ evento di rete FD xxx (ad esempio, \_ lettura FD e \_ scrittura FD), viene impostato un oggetto evento designato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5059-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="f5059-107">Inoltre, il fatto che si \_ sia verificato un evento di rete FD XXX specifico viene memorizzato dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f5059-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="f5059-108">L'applicazione può chiamare [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) per fare in modo che il contenuto corrente della memoria degli eventi di rete venga copiato in un buffer fornito dall'applicazione e che la memoria dell'evento di rete venga cancellata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f5059-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="f5059-109">Se necessario, l'applicazione può anche designare un particolare oggetto evento che viene cancellato insieme alla memoria dell'evento di rete.</span><span class="sxs-lookup"><span data-stu-id="f5059-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



