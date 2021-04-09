---
description: I programmatori e gli amministratori di sistema utilizzano i programmi di configurazione del servizio per modificare o eseguire query sul database dei servizi installati.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programmi di configurazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128898"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="374ca-103">Programmi di configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="374ca-103">Service Configuration Programs</span></span>

<span data-ttu-id="374ca-104">I programmatori e gli amministratori di sistema utilizzano i programmi di configurazione del servizio per modificare o eseguire query sul database dei servizi installati.</span><span class="sxs-lookup"><span data-stu-id="374ca-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="374ca-105">È possibile accedere al database anche usando le funzioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="374ca-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="374ca-106">Tuttavia, è consigliabile usare solo le funzioni di configurazione SCM, che assicurano che il servizio sia installato e configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="374ca-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="374ca-107">Le funzioni di configurazione SCM richiedono un handle per un oggetto SCManager o un handle per un oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="374ca-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="374ca-108">Per ottenere questi handle, il programma di configurazione del servizio deve:</span><span class="sxs-lookup"><span data-stu-id="374ca-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="374ca-109">Utilizzare la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per ottenere un handle per il database SCM in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="374ca-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="374ca-110">Utilizzare la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per ottenere un handle per l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="374ca-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="374ca-111">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="374ca-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="374ca-112">Installazione, rimozione ed enumerazione del servizio</span><span class="sxs-lookup"><span data-stu-id="374ca-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="374ca-113">Configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="374ca-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="374ca-114">Configurazione di un servizio con SC</span><span class="sxs-lookup"><span data-stu-id="374ca-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 



