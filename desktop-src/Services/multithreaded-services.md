---
description: Gestione controllo servizi (SCM) controlla un servizio inviando eventi di controllo del servizio alla routine del gestore di controllo dei servizi.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Servizi multithreading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316615"
---
# <a name="multithreaded-services"></a><span data-ttu-id="3d3bf-103">Servizi multithreading</span><span class="sxs-lookup"><span data-stu-id="3d3bf-103">Multithreaded Services</span></span>

<span data-ttu-id="3d3bf-104">Gestione controllo servizi (SCM) controlla un servizio inviando eventi di controllo del servizio alla routine del gestore di controllo del servizio.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="3d3bf-105">Il servizio deve rispondere per controllare gli eventi in modo tempestivo, in modo che SCM possa tenere traccia dello stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="3d3bf-106">Inoltre, lo stato del servizio deve corrispondere alla descrizione dello stato ricevuto dall'SCM.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="3d3bf-107">A causa di questo meccanismo di comunicazione tra un servizio e il controllo SCM, è necessario prestare attenzione quando si usano più thread in un servizio.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="3d3bf-108">Quando a un servizio viene richiesto di arrestare il servizio SCM, è necessario attendere la chiusura di tutti i thread prima di segnalare al gestore SCM che il servizio è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="3d3bf-109">In caso contrario, il controllo SCM può diventare confuso sullo stato del servizio e potrebbe non riuscire a arrestarsi correttamente.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="3d3bf-110">Il servizio SCM deve ricevere una notifica che indica che il servizio sta rispondendo all'evento di arresto del controllo e che lo stato di avanzamento viene eseguito durante l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="3d3bf-111">Il servizio SCM presuppone che il servizio sia in corso se il servizio risponde (tramite [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) entro l'intervallo di tempo (hint di attesa) specificato nella precedente chiamata a **SetServiceStatus** e il punto di controllo viene aggiornato in modo che sia maggiore del checkpoint specificato nella precedente chiamata a **SetServiceStatus**.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="3d3bf-112">Se il servizio segnala al gestore SCM che il servizio è stato arrestato prima della chiusura di tutti i thread, è possibile che SCM interpreti questa operazione come una contraddizione.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="3d3bf-113">Questo potrebbe causare uno stato in cui il servizio non può essere arrestato o riavviato.</span><span class="sxs-lookup"><span data-stu-id="3d3bf-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 



