---
description: Gestione controllo servizi viene avviato all'avvio del sistema. Si tratta di un server RPC (Remote Procedure Call), in modo che i programmi di configurazione del servizio e di controllo del servizio possano modificare i servizi in computer remoti.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gestione controllo servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306534"
---
# <a name="service-control-manager"></a><span data-ttu-id="9f472-104">Gestione controllo servizi</span><span class="sxs-lookup"><span data-stu-id="9f472-104">Service Control Manager</span></span>

<span data-ttu-id="9f472-105">Gestione controllo servizi viene avviato all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="9f472-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="9f472-106">Si tratta di un server RPC (Remote Procedure Call), in modo che i programmi di configurazione del servizio e di controllo del servizio possano modificare i servizi in computer remoti.</span><span class="sxs-lookup"><span data-stu-id="9f472-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="9f472-107">Le funzioni del servizio forniscono un'interfaccia per le seguenti attività eseguite da SCM:</span><span class="sxs-lookup"><span data-stu-id="9f472-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="9f472-108">Gestione del database dei servizi installati.</span><span class="sxs-lookup"><span data-stu-id="9f472-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="9f472-109">Avvio di servizi e servizi di driver all'avvio del sistema o su richiesta.</span><span class="sxs-lookup"><span data-stu-id="9f472-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="9f472-110">Enumerazione dei servizi installati e dei servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="9f472-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="9f472-111">Gestione delle informazioni sullo stato per l'esecuzione dei servizi e dei servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="9f472-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="9f472-112">Trasmissione di richieste di controllo ai servizi in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9f472-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="9f472-113">Bloccare e sbloccare il database del servizio.</span><span class="sxs-lookup"><span data-stu-id="9f472-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="9f472-114">Le sezioni seguenti descrivono il controllo SCM in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="9f472-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="9f472-115">Database dei servizi installati</span><span class="sxs-lookup"><span data-stu-id="9f472-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="9f472-116">Avvio automatico dei servizi</span><span class="sxs-lookup"><span data-stu-id="9f472-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="9f472-117">Avvio dei servizi su richiesta</span><span class="sxs-lookup"><span data-stu-id="9f472-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="9f472-118">Elenco di record di servizio</span><span class="sxs-lookup"><span data-stu-id="9f472-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="9f472-119">Handle SCM</span><span class="sxs-lookup"><span data-stu-id="9f472-119">SCM Handles</span></span>](scm-handles.md)

 

 



