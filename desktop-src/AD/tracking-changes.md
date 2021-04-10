---
title: Rilevamento delle modifiche
description: Alcune applicazioni devono mantenere la coerenza tra dati specifici archiviati nel servizio directory Active Directory e altri dati.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, rilevamento delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956296"
---
# <a name="tracking-changes"></a><span data-ttu-id="7ba05-104">Rilevamento delle modifiche</span><span class="sxs-lookup"><span data-stu-id="7ba05-104">Tracking Changes</span></span>

<span data-ttu-id="7ba05-105">Alcune applicazioni devono mantenere la coerenza tra dati specifici archiviati nel servizio directory Active Directory e altri dati.</span><span class="sxs-lookup"><span data-stu-id="7ba05-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="7ba05-106">Gli altri dati potrebbero essere archiviati nella directory, in una tabella SQL Server, in un file o nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ba05-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="7ba05-107">Quando i dati archiviati nella directory cambiano, è possibile che gli altri dati vengano modificati per rimanere coerenti.</span><span class="sxs-lookup"><span data-stu-id="7ba05-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="7ba05-108">Le applicazioni che presentano questo requisito includono:</span><span class="sxs-lookup"><span data-stu-id="7ba05-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="7ba05-109">Questa sezione non include i meccanismi usati per il monitoraggio delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7ba05-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="7ba05-110">Si tratta di applicazioni che eseguono il monitoraggio delle modifiche della directory non allo scopo di gestire dati coerenti tra archivi distinti, ma come strumento di gestione del sistema.</span><span class="sxs-lookup"><span data-stu-id="7ba05-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="7ba05-111">Sebbene le applicazioni di monitoraggio possano utilizzare gli stessi meccanismi che supportano le applicazioni di rilevamento delle modifiche, i meccanismi seguenti sono appositamente progettati per il monitoraggio delle applicazioni:</span><span class="sxs-lookup"><span data-stu-id="7ba05-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="7ba05-112">Controllo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7ba05-112">Security auditing.</span></span> <span data-ttu-id="7ba05-113">Modificando la parte dell'elenco di controllo di accesso di sistema (SACL) di un descrittore di sicurezza di un oggetto, è possibile fare in modo che gli accessi all'oggetto in un determinato controller di dominio creino record di controllo nel registro eventi di protezione.</span><span class="sxs-lookup"><span data-stu-id="7ba05-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="7ba05-114">È possibile controllare le letture, le Scritture o entrambe le operazioni; è possibile controllare l'intero oggetto o attributi specifici.</span><span class="sxs-lookup"><span data-stu-id="7ba05-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="7ba05-115">Per altre informazioni, vedere [recupero del SACL di un oggetto](retrieving-an-objectampaposs-sacl.md) e [generazione del controllo](/windows/desktop/SecAuthZ/audit-generation).</span><span class="sxs-lookup"><span data-stu-id="7ba05-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="7ba05-116">Registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="7ba05-116">Event logging.</span></span> <span data-ttu-id="7ba05-117">Modificando le impostazioni del registro di sistema in un controller di dominio specifico, è possibile modificare i tipi di eventi registrati nel registro eventi del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="7ba05-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="7ba05-118">In particolare, per registrare tutte le modifiche, impostare il valore di **accesso alla directory 8** sotto la chiave del registro di sistema seguente su 4.</span><span class="sxs-lookup"><span data-stu-id="7ba05-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="7ba05-119">Per ulteriori informazioni, vedere [registrazione degli eventi](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="7ba05-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="7ba05-120">Traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="7ba05-120">Event tracing.</span></span> <span data-ttu-id="7ba05-121">In Windows 2000 è stata introdotta un'API di traccia eventi per la traccia e la registrazione di eventi interessanti in software o hardware.</span><span class="sxs-lookup"><span data-stu-id="7ba05-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="7ba05-122">Il sistema operativo Windows e Active Directory Domain Services in particolare supportano l'utilizzo di traccia eventi per la pianificazione della capacità e l'analisi dettagliata delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7ba05-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="7ba05-123">Per ulteriori informazioni, vedere [traccia eventi](/windows/desktop/ETW/event-tracing-portal) e [traccia eventi in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span><span class="sxs-lookup"><span data-stu-id="7ba05-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="7ba05-124">Questa sezione include gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba05-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="7ba05-125">Cenni preliminari sulle tecniche di Rilevamento modifiche</span><span class="sxs-lookup"><span data-stu-id="7ba05-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="7ba05-126">Modificare le notifiche in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7ba05-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="7ba05-127">Polling delle modifiche tramite il controllo DirSync</span><span class="sxs-lookup"><span data-stu-id="7ba05-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="7ba05-128">Polling delle modifiche tramite USNChanged</span><span class="sxs-lookup"><span data-stu-id="7ba05-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 