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
# <a name="about-event-logging"></a><span data-ttu-id="d1cb6-103">Informazioni sulla registrazione degli eventi</span><span class="sxs-lookup"><span data-stu-id="d1cb6-103">About Event Logging</span></span>

<span data-ttu-id="d1cb6-104">Quando si verifica un errore, l'amministratore di sistema o il rappresentante del supporto tecnico deve determinare la causa dell'errore, tentare di recuperare i dati persi ed evitare che si verifichi un errore.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="d1cb6-105">È utile se le applicazioni, il sistema operativo e altri servizi di sistema registrano eventi importanti, ad esempio le condizioni di memoria insufficiente o un numero eccessivo di tentativi di accesso a un disco.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="d1cb6-106">L'amministratore di sistema può quindi utilizzare il registro eventi per determinare le condizioni che hanno causato l'errore e identificare il contesto in cui si è verificato.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="d1cb6-107">Visualizzando periodicamente il registro eventi, l'amministratore di sistema potrebbe essere in grado di identificare i problemi, ad esempio un disco rigido guasto, prima che causino danni.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="d1cb6-108">L'API di registrazione eventi è stata progettata per le applicazioni eseguite nel sistema operativo Windows Server 2003, Windows XP o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="d1cb6-109">In Windows Vista, l'infrastruttura di registrazione degli eventi è stata riprogettata.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="d1cb6-110">Le applicazioni progettate per l'esecuzione nei sistemi operativi Windows Vista o versioni successive dovrebbero ora usare il [registro eventi di Windows](/windows/desktop/WES/windows-event-log) per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="d1cb6-111">In questa sezione viene illustrata l'interfaccia di programmazione per la scrittura e l'utilizzo di eventi mediante la registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="d1cb6-112">Tipi di evento</span><span class="sxs-lookup"><span data-stu-id="d1cb6-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="d1cb6-113">Linee guida per la registrazione</span><span class="sxs-lookup"><span data-stu-id="d1cb6-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="d1cb6-114">Elementi di registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="d1cb6-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="d1cb6-115">Operazioni di registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="d1cb6-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="d1cb6-116">Modello di registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="d1cb6-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="d1cb6-117">Sicurezza registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="d1cb6-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="d1cb6-118">Le applicazioni che pubblicano eventi di dimensioni superiori a 64 kilobyte in un computer Windows Server 2003, Windows XP o Windows 2000 non saranno in grado di pubblicare eventi in un computer Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d1cb6-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
