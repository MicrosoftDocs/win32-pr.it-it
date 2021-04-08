---
title: Ripristino e riavvio di un'applicazione
description: Scrivere programmi di installazione personalizzati per riavviare automaticamente un'applicazione che è stata arrestata per completare un aggiornamento. Salvare i dati e configurare il ripristino dell'applicazione prima di chiudere i programmi.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- affidabilità
- affidabilità software
- ripristino dell'applicazione
- riavvio dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856802"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="4ad19-111">Ripristino e riavvio di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="4ad19-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="4ad19-112">Scopo</span><span class="sxs-lookup"><span data-stu-id="4ad19-112">Purpose</span></span>

<span data-ttu-id="4ad19-113">Un'applicazione può usare il ripristino e il riavvio dell'applicazione (ARR) per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere.</span><span class="sxs-lookup"><span data-stu-id="4ad19-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="4ad19-114">Se richiesto, viene riavviata anche l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ad19-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="4ad19-115">Un'applicazione può essere riavviata anche se un programma di installazione aggiorna un componente dell'applicazione o se il computer deve essere riavviato come risultato di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4ad19-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="4ad19-116">Si noti che per supportare il riavvio automatico dell'applicazione dopo l'aggiornamento di un'applicazione da parte di un programma di installazione, è necessario creare l'applicazione e il programma di installazione in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="4ad19-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="4ad19-117">Per informazioni dettagliate, vedere [la pagina relativa alla registrazione per il riavvio dell'applicazione](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="4ad19-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4ad19-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="4ad19-118">Developer audience</span></span>

<span data-ttu-id="4ad19-119">ARR è progettato per gli sviluppatori C e C++.</span><span class="sxs-lookup"><span data-stu-id="4ad19-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4ad19-120">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="4ad19-120">Run-time requirements</span></span>

<span data-ttu-id="4ad19-121">ARR è disponibile a partire dal sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ad19-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4ad19-122">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4ad19-122">In this section</span></span>



| <span data-ttu-id="4ad19-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="4ad19-123">Topic</span></span>                                                                                                   | <span data-ttu-id="4ad19-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ad19-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="4ad19-125">Utilizzo del ripristino dell'applicazione e riavvio</span><span class="sxs-lookup"><span data-stu-id="4ad19-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="4ad19-126">Guida procedurale per la registrazione per il ripristino e il riavvio.</span><span class="sxs-lookup"><span data-stu-id="4ad19-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="4ad19-127">Riferimento al ripristino e al riavvio dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="4ad19-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="4ad19-128">Informazioni di riferimento per l'API ARR.</span><span class="sxs-lookup"><span data-stu-id="4ad19-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





