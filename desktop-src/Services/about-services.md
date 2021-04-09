---
description: Gestione controllo servizi gestisce un database di servizi e driver installati e fornisce un mezzo unificato e sicuro per controllarli.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Informazioni sui servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967869"
---
# <a name="about-services"></a><span data-ttu-id="52efd-103">Informazioni sui servizi</span><span class="sxs-lookup"><span data-stu-id="52efd-103">About Services</span></span>

<span data-ttu-id="52efd-104">[Gestione controllo servizi](service-control-manager.md) gestisce un database di servizi e driver installati e fornisce un mezzo unificato e sicuro per controllarli.</span><span class="sxs-lookup"><span data-stu-id="52efd-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="52efd-105">Nel database sono incluse informazioni sulla modalità di avvio di ogni servizio o servizio driver.</span><span class="sxs-lookup"><span data-stu-id="52efd-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="52efd-106">Consente inoltre agli amministratori di sistema di personalizzare i requisiti di sicurezza per ogni servizio e quindi di controllare l'accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="52efd-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="52efd-107">I tipi di programmi seguenti usano le funzioni fornite da SCM.</span><span class="sxs-lookup"><span data-stu-id="52efd-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="52efd-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="52efd-108">Type</span></span>                          | <span data-ttu-id="52efd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52efd-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52efd-110">Programma del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-110">Service program</span></span>               | <span data-ttu-id="52efd-111">Programma che fornisce codice eseguibile per uno o più servizi.</span><span class="sxs-lookup"><span data-stu-id="52efd-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="52efd-112">I programmi di servizio utilizzano funzioni che si connettono a SCM e inviano informazioni sullo stato a SCM.</span><span class="sxs-lookup"><span data-stu-id="52efd-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="52efd-113">Programma di configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-113">Service configuration program</span></span> | <span data-ttu-id="52efd-114">Programma che esegue query o modifica il database dei servizi.</span><span class="sxs-lookup"><span data-stu-id="52efd-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="52efd-115">I programmi di configurazione dei servizi utilizzano funzioni che aprono il database, installano o eliminano i servizi nel database ed eseguono query o modificano i parametri di configurazione e di sicurezza per i servizi installati.</span><span class="sxs-lookup"><span data-stu-id="52efd-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="52efd-116">I programmi di configurazione dei servizi gestiscono sia servizi che servizi driver.</span><span class="sxs-lookup"><span data-stu-id="52efd-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="52efd-117">Programma di controllo del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-117">Service control program</span></span>       | <span data-ttu-id="52efd-118">Programma che avvia e controlla i servizi e i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="52efd-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="52efd-119">I programmi di controllo del servizio usano funzioni che inviano richieste a SCM, che esegue la richiesta.</span><span class="sxs-lookup"><span data-stu-id="52efd-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="52efd-120">In questa panoramica vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="52efd-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="52efd-121">Gestione controllo servizi</span><span class="sxs-lookup"><span data-stu-id="52efd-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="52efd-122">Programmi di servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="52efd-123">Programmi di configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="52efd-124">Programmi di controllo del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="52efd-125">Account utente del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="52efd-126">Servizi interattivi</span><span class="sxs-lookup"><span data-stu-id="52efd-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="52efd-127">Sicurezza del servizio e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="52efd-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="52efd-128">Debug di un servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="52efd-129">Eventi trigger del servizio</span><span class="sxs-lookup"><span data-stu-id="52efd-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



