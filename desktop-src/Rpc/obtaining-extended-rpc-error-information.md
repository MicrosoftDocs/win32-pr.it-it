---
title: Recupero delle informazioni sull'errore RPC esteso
description: RPC fornisce la possibilità di ottenere informazioni estese sull'errore. Questa sezione descrive il modo in cui è possibile ottenere tali informazioni sugli errori e offre consigli su come usare le informazioni.
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- RPC (Remote Procedure Call), procedure consigliate, informazioni estese sugli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710417"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="efbb6-105">Recupero delle informazioni sull'errore RPC esteso</span><span class="sxs-lookup"><span data-stu-id="efbb6-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="efbb6-106">RPC fornisce la possibilità di ottenere informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="efbb6-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="efbb6-107">Questa sezione descrive il modo in cui è possibile ottenere tali informazioni sugli errori e offre consigli su come usare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="efbb6-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="efbb6-108">Questa sezione è suddivisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="efbb6-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="efbb6-109">Necessità di informazioni estese sugli errori</span><span class="sxs-lookup"><span data-stu-id="efbb6-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="efbb6-110">Informazioni sulla sicurezza e sugli errori estesi</span><span class="sxs-lookup"><span data-stu-id="efbb6-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="efbb6-111">Abilitazione di informazioni estese sugli errori</span><span class="sxs-lookup"><span data-stu-id="efbb6-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="efbb6-112">Informazioni sugli errori estesi</span><span class="sxs-lookup"><span data-stu-id="efbb6-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="efbb6-113">Affidabilità delle informazioni estese sugli errori</span><span class="sxs-lookup"><span data-stu-id="efbb6-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="efbb6-114">Indipendenza da altri componenti</span><span class="sxs-lookup"><span data-stu-id="efbb6-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="efbb6-115">Informazioni estese sull'errore per l'utente</span><span class="sxs-lookup"><span data-stu-id="efbb6-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="efbb6-116">Informazioni estese sull'errore per il server o l'applicazione</span><span class="sxs-lookup"><span data-stu-id="efbb6-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="efbb6-117">Percorsi di rilevamento delle informazioni sugli errori estesi</span><span class="sxs-lookup"><span data-stu-id="efbb6-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="efbb6-118">Questa sezione è strettamente legata al debug dell'applicazione RPC.</span><span class="sxs-lookup"><span data-stu-id="efbb6-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="efbb6-119">Per ulteriori informazioni sul debug RPC, vedere \[ pacchetto del debugger \] .</span><span class="sxs-lookup"><span data-stu-id="efbb6-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




