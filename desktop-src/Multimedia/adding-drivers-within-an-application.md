---
title: Aggiunta di driver all'interno di un'applicazione
description: Aggiunta di driver all'interno di un'applicazione
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Gestione compressione audio (ACM), aggiunta di driver
- ACM (Gestione compressione audio), aggiunta di driver
- Esempi di ACM, aggiunta di driver
- Aggiunta di driver
- acmDriverAdd (funzione)
- driver globali
- driver locali
- Gestione compressione audio (ACM), driver globali
- ACM (Gestione compressione audio), driver globali
- Gestione compressione audio (ACM), driver locali
- ACM (Gestione compressione audio), driver locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044730"
---
# <a name="adding-drivers-within-an-application"></a><span data-ttu-id="daa1b-114">Aggiunta di driver all'interno di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="daa1b-114">Adding Drivers Within an Application</span></span>

<span data-ttu-id="daa1b-115">Se è necessario che l'applicazione implementi le proprie routine di compressione internamente, l'applicazione può aggiungere driver all'ACM chiamando la funzione [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="daa1b-115">If you need your application to implement its own compression routines internally, the application can add drivers to the ACM by calling the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span> <span data-ttu-id="daa1b-116">L'applicazione implementa il driver fornendo una funzione conforme al prototipo [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="daa1b-116">The application implements the driver by providing a function that conforms to the [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) prototype.</span></span> <span data-ttu-id="daa1b-117">Dopo che l'applicazione ha aggiunto il driver, l'applicazione può utilizzare il driver tramite l'ACM, perché utilizzerebbe qualsiasi altro driver.</span><span class="sxs-lookup"><span data-stu-id="daa1b-117">After the application has added the driver, the application can use the driver through the ACM as it would use any other driver.</span></span>

<span data-ttu-id="daa1b-118">L'ACM considera i driver come globali o locali.</span><span class="sxs-lookup"><span data-stu-id="daa1b-118">The ACM treats drivers as either global or local.</span></span> <span data-ttu-id="daa1b-119">Un'applicazione specifica se un driver deve essere aggiunto come globale o locale quando chiama **acmDriverAdd**.</span><span class="sxs-lookup"><span data-stu-id="daa1b-119">An application specifies whether a driver should be added as global or local when it calls **acmDriverAdd**.</span></span> <span data-ttu-id="daa1b-120">Esistono due differenze tra i driver globali e locali:</span><span class="sxs-lookup"><span data-stu-id="daa1b-120">There are two differences between global and local drivers:</span></span>

-   <span data-ttu-id="daa1b-121">I driver aggiunti come driver globali non sono condivisi con altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="daa1b-121">Drivers added as global drivers are not shared with other applications.</span></span>
-   <span data-ttu-id="daa1b-122">Un'applicazione può modificare direttamente la priorità di un driver globale, ma non di un driver locale, chiamando la funzione [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) .</span><span class="sxs-lookup"><span data-stu-id="daa1b-122">An application can directly alter the priority of a global driver (but not a local driver) by calling the [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) function.</span></span> <span data-ttu-id="daa1b-123">L'ACM esegue una ricerca con priorità durante la ricerca di un driver appropriato per fornire un'implementazione di una chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="daa1b-123">The ACM conducts a prioritized search when seeking an appropriate driver to provide an implementation of a function call.</span></span> <span data-ttu-id="daa1b-124">L'ACM assegna sempre ai driver locali una priorità più alta rispetto ai driver globali.</span><span class="sxs-lookup"><span data-stu-id="daa1b-124">The ACM always gives local drivers higher priority than global drivers.</span></span> <span data-ttu-id="daa1b-125">Il driver locale aggiunto più di recente ha la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="daa1b-125">The most recently added local driver has highest priority.</span></span>

 

 




