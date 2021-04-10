---
description: Un programma del servizio contiene codice eseguibile per uno o più servizi.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programmi di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884830"
---
# <a name="service-programs"></a><span data-ttu-id="70aa0-103">Programmi di servizio</span><span class="sxs-lookup"><span data-stu-id="70aa0-103">Service Programs</span></span>

<span data-ttu-id="70aa0-104">Un *programma del servizio* contiene codice eseguibile per uno o più servizi.</span><span class="sxs-lookup"><span data-stu-id="70aa0-104">A *service program* contains executable code for one or more services.</span></span> <span data-ttu-id="70aa0-105">Un programma di servizio creato con il processo del servizio di tipo \_ Win32 \_ own \_ contiene il codice per un solo servizio.</span><span class="sxs-lookup"><span data-stu-id="70aa0-105">A service program created with the type SERVICE\_WIN32\_OWN\_PROCESS contains the code for only one service.</span></span> <span data-ttu-id="70aa0-106">Un programma di servizio creato con il \_ processo di condivisione Win32 del servizio di tipo contiene il \_ \_ codice per più di un servizio, consentendo loro di condividere il codice.</span><span class="sxs-lookup"><span data-stu-id="70aa0-106">A service program created with the type SERVICE\_WIN32\_SHARE\_PROCESS contains code for more than one service, enabling them to share code.</span></span> <span data-ttu-id="70aa0-107">Un esempio di un programma di servizio che esegue questa operazione è il processo host del servizio generico, Svchost.exe, che ospita servizi Windows interni.</span><span class="sxs-lookup"><span data-stu-id="70aa0-107">An example of a service program that does this is the generic service host process, Svchost.exe, which hosts internal Windows services.</span></span> <span data-ttu-id="70aa0-108">Si noti che Svchost.exe è riservata per l'utilizzo da parte del sistema operativo e non deve essere utilizzata da servizi non Windows.</span><span class="sxs-lookup"><span data-stu-id="70aa0-108">Note that Svchost.exe is reserved for use by the operating system and should not be used by non-Windows services.</span></span> <span data-ttu-id="70aa0-109">Gli sviluppatori devono invece implementare i propri programmi di hosting dei servizi.</span><span class="sxs-lookup"><span data-stu-id="70aa0-109">Instead, developers should implement their own service hosting programs.</span></span>

<span data-ttu-id="70aa0-110">Un programma del servizio può essere configurato per l'esecuzione nel contesto di un account utente dal dominio predefinito (locale), primario o attendibile.</span><span class="sxs-lookup"><span data-stu-id="70aa0-110">A service program can be configured to execute in the context of a user account from either the built-in (local), primary, or trusted domain.</span></span> <span data-ttu-id="70aa0-111">Può anche essere configurato per l'esecuzione in un [account utente di servizio](service-user-accounts.md)speciale.</span><span class="sxs-lookup"><span data-stu-id="70aa0-111">It can also be configured to run in a special [service user account](service-user-accounts.md).</span></span>

<span data-ttu-id="70aa0-112">Negli argomenti seguenti vengono descritti i requisiti di interfaccia di [Gestione controllo servizi](service-control-manager.md) (SCM) che un programma del servizio deve includere:</span><span class="sxs-lookup"><span data-stu-id="70aa0-112">The following topics describe the interface requirements of the [service control manager](service-control-manager.md) (SCM) that a service program must include:</span></span>

-   [<span data-ttu-id="70aa0-113">Punto di ingresso del servizio</span><span class="sxs-lookup"><span data-stu-id="70aa0-113">Service Entry Point</span></span>](service-entry-point.md)
-   [<span data-ttu-id="70aa0-114">Funzione ServiceMain del servizio</span><span class="sxs-lookup"><span data-stu-id="70aa0-114">Service ServiceMain Function</span></span>](service-servicemain-function.md)
-   [<span data-ttu-id="70aa0-115">Funzione Handler di controllo dei servizi</span><span class="sxs-lookup"><span data-stu-id="70aa0-115">Service Control Handler Function</span></span>](service-control-handler-function.md)

<span data-ttu-id="70aa0-116">Questi argomenti non si applicano ai servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="70aa0-116">These topics do not apply to driver services.</span></span> <span data-ttu-id="70aa0-117">Per informazioni sui requisiti di interfaccia dei servizi driver, vedere Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="70aa0-117">For interface requirements of driver services, see the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="70aa0-118">Un servizio viene eseguito come processo in background che può influire sulle prestazioni del sistema, sulla velocità di risposta, sull'efficienza energetica e sulla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="70aa0-118">A service runs as a background process that can affect system performance, responsiveness, energy efficiency, and security.</span></span> <span data-ttu-id="70aa0-119">Per le linee guida sull'ottimizzazione dei servizi, vedere [sviluppo di processi in background efficienti per Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span><span class="sxs-lookup"><span data-stu-id="70aa0-119">For service optimization guidelines, see [Developing Efficient Background Processes for Windows](/windows-hardware/drivers/kernel/implementing-power-management).</span></span> <span data-ttu-id="70aa0-120">Gli argomenti seguenti descrivono considerazioni aggiuntive sulla programmazione:</span><span class="sxs-lookup"><span data-stu-id="70aa0-120">The following topics describe additional programming considerations:</span></span>

-   [<span data-ttu-id="70aa0-121">Transizioni di stato del servizio</span><span class="sxs-lookup"><span data-stu-id="70aa0-121">Service State Transitions</span></span>](service-status-transitions.md)
-   [<span data-ttu-id="70aa0-122">Ricezione di eventi in un servizio</span><span class="sxs-lookup"><span data-stu-id="70aa0-122">Receiving Events in a Service</span></span>](receiving-events-in-a-service.md)
-   [<span data-ttu-id="70aa0-123">Servizi multithreading</span><span class="sxs-lookup"><span data-stu-id="70aa0-123">Multithreaded Services</span></span>](multithreaded-services.md)
-   [<span data-ttu-id="70aa0-124">Servizi e registro di sistema</span><span class="sxs-lookup"><span data-stu-id="70aa0-124">Services and the Registry</span></span>](services-and-the-registry.md)
-   [<span data-ttu-id="70aa0-125">Servizi e unità reindirizzate</span><span class="sxs-lookup"><span data-stu-id="70aa0-125">Services and Redirected Drives</span></span>](services-and-redirected-drives.md)
-   [<span data-ttu-id="70aa0-126">Eventi trigger del servizio</span><span class="sxs-lookup"><span data-stu-id="70aa0-126">Service Trigger Events</span></span>](service-trigger-events.md)

<span data-ttu-id="70aa0-127">Si noti che se il programma del servizio funziona come server RPC, deve usare endpoint dinamici e l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="70aa0-127">Note that if the service program functions as an RPC server, it should use dynamic endpoints and mutual authentication.</span></span>

 

 
