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
# <a name="event-logging-event-logging"></a><span data-ttu-id="f5ea4-103">Registrazione eventi (registrazione eventi)</span><span class="sxs-lookup"><span data-stu-id="f5ea4-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="f5ea4-104">Molte applicazioni registrano gli errori e gli eventi nei log degli errori proprietari, ognuno con il proprio formato e l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="f5ea4-105">Non è possibile unire facilmente i dati di applicazioni diverse in un unico report completo, in modo da richiedere agli amministratori di sistema o ai rappresentanti del supporto tecnico di controllare un'ampia gamma di origini per diagnosticare i problemi.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="f5ea4-106">La registrazione degli eventi fornisce un metodo standard e centralizzato per le applicazioni (e il sistema operativo) per la registrazione di importanti eventi software e hardware.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="f5ea4-107">Il servizio di registrazione eventi registra gli eventi da diverse origini e li archivia in una singola raccolta denominata *log eventi*.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="f5ea4-108">Il Visualizzatore eventi consente di visualizzare i log. l'interfaccia di programmazione consente inoltre di esaminare i log.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="f5ea4-109">Informazioni sulla registrazione degli eventi</span><span class="sxs-lookup"><span data-stu-id="f5ea4-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="f5ea4-110">Uso della registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="f5ea4-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="f5ea4-111">Riferimento per la registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="f5ea4-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="f5ea4-112">L'API di registrazione eventi è stata progettata per le applicazioni eseguite nel sistema operativo Windows Server 2003, Windows XP o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="f5ea4-113">In Windows Vista, l'infrastruttura di registrazione degli eventi è stata riprogettata.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="f5ea4-114">Le applicazioni progettate per l'esecuzione in Windows Vista o sistemi operativi successivi devono usare il [registro eventi di Windows](/windows/desktop/WES/windows-event-log) per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>
