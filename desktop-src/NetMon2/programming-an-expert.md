---
description: Il Network Monitor SDK include le funzioni e il codice di esempio necessari per compilare esperti. Tuttavia, è anche possibile usare gli strumenti esistenti, incluso un editor di finestre.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programmazione di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131462"
---
# <a name="programming-an-expert"></a><span data-ttu-id="df0ce-104">Programmazione di un esperto</span><span class="sxs-lookup"><span data-stu-id="df0ce-104">Programming an Expert</span></span>

<span data-ttu-id="df0ce-105">Il Network Monitor SDK include le funzioni e il codice di esempio necessari per compilare esperti.</span><span class="sxs-lookup"><span data-stu-id="df0ce-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="df0ce-106">Tuttavia, è anche possibile usare gli strumenti esistenti, incluso un editor di finestre.</span><span class="sxs-lookup"><span data-stu-id="df0ce-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="df0ce-107">Requisiti minimi per l'esecuzione di un esperto</span><span class="sxs-lookup"><span data-stu-id="df0ce-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="df0ce-108">Nella tabella seguente sono elencati i punti di ingresso della DLL e le funzioni esperte che è necessario utilizzare per compilare un esperto.</span><span class="sxs-lookup"><span data-stu-id="df0ce-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="df0ce-109">Nome</span><span class="sxs-lookup"><span data-stu-id="df0ce-109">Name</span></span>                                                 | <span data-ttu-id="df0ce-110">Type</span><span class="sxs-lookup"><span data-stu-id="df0ce-110">Type</span></span>               | <span data-ttu-id="df0ce-111">Obbligatorio?</span><span class="sxs-lookup"><span data-stu-id="df0ce-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="df0ce-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="df0ce-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="df0ce-113">Funzione voce DLL</span><span class="sxs-lookup"><span data-stu-id="df0ce-113">DLL entry function</span></span> | <span data-ttu-id="df0ce-114">Sì</span><span class="sxs-lookup"><span data-stu-id="df0ce-114">Yes</span></span>                                             |
| [<span data-ttu-id="df0ce-115">**Registra esperto**</span><span class="sxs-lookup"><span data-stu-id="df0ce-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="df0ce-116">Funzione voce DLL</span><span class="sxs-lookup"><span data-stu-id="df0ce-116">DLL entry function</span></span> | <span data-ttu-id="df0ce-117">Sì</span><span class="sxs-lookup"><span data-stu-id="df0ce-117">Yes</span></span>                                             |
| [<span data-ttu-id="df0ce-118">**Correre**</span><span class="sxs-lookup"><span data-stu-id="df0ce-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="df0ce-119">Funzione voce DLL</span><span class="sxs-lookup"><span data-stu-id="df0ce-119">DLL entry function</span></span> | <span data-ttu-id="df0ce-120">Sì</span><span class="sxs-lookup"><span data-stu-id="df0ce-120">Yes</span></span>                                             |
| [<span data-ttu-id="df0ce-121">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="df0ce-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="df0ce-122">Funzione voce DLL</span><span class="sxs-lookup"><span data-stu-id="df0ce-122">DLL entry function</span></span> | <span data-ttu-id="df0ce-123">Solo se l'esperto fornisce la configurazione utente.</span><span class="sxs-lookup"><span data-stu-id="df0ce-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="df0ce-124">**ExpertIndicateStatus**</span><span class="sxs-lookup"><span data-stu-id="df0ce-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="df0ce-125">Funzione Expert</span><span class="sxs-lookup"><span data-stu-id="df0ce-125">Expert function</span></span>    | <span data-ttu-id="df0ce-126">Sì</span><span class="sxs-lookup"><span data-stu-id="df0ce-126">Yes</span></span>                                             |
| [<span data-ttu-id="df0ce-127">**ExpertSubmitEvent**</span><span class="sxs-lookup"><span data-stu-id="df0ce-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="df0ce-128">Funzione Expert</span><span class="sxs-lookup"><span data-stu-id="df0ce-128">Expert function</span></span>    | <span data-ttu-id="df0ce-129">Sì</span><span class="sxs-lookup"><span data-stu-id="df0ce-129">Yes</span></span>                                             |



 

<span data-ttu-id="df0ce-130">Esaminare gli argomenti di riferimento per esperti e parser nell'SDK di Network Monitor per aggiornare il codice sorgente e quindi usare il codice di esempio e le procedure fornite negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="df0ce-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="df0ce-131">Creazione di un esperto</span><span class="sxs-lookup"><span data-stu-id="df0ce-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="df0ce-132">Installazione di un esperto</span><span class="sxs-lookup"><span data-stu-id="df0ce-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="df0ce-133">Debug di un esperto</span><span class="sxs-lookup"><span data-stu-id="df0ce-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="df0ce-134">Per le DLL di esperti è richiesta la convenzione di chiamata C, non C++, perché le funzioni vengono chiamate tramite puntatori a funzione tramite un overlay.</span><span class="sxs-lookup"><span data-stu-id="df0ce-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="df0ce-135">Tramite un set di funzioni esperte specializzate, l'esperto può accedere ai frame nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="df0ce-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="df0ce-136">L'esperto può utilizzare la maggior parte delle Network Monitor API per modificare i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="df0ce-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="df0ce-137">Quando un esperto trova le informazioni da inviare all'utente, le informazioni vengono composte in una struttura di dati degli eventi e inviate a Network Monitor, che quindi Visualizza le informazioni in una finestra di output esperta.</span><span class="sxs-lookup"><span data-stu-id="df0ce-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="df0ce-138">L'esperto deve aggiornare periodicamente Network Monitor con informazioni sullo stato di completamento percentuale, fornito dalla funzione [**ExpertIndicateStatus**](expertindicatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="df0ce-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="df0ce-139">Le funzioni esportate dell'esperto vengono chiamate come segue:</span><span class="sxs-lookup"><span data-stu-id="df0ce-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="df0ce-140">Quando Network Monitor crea l'elenco di esperti da presentare all'utente, Network Monitor chiama la funzione [**Register Expert**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="df0ce-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="df0ce-141">Dopo la chiamata a **Register**, se l'esperto è configurabile, Network Monitor chiama la funzione [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="df0ce-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="df0ce-142">Quando l'utente Network Monitor fa clic su **Esegui esperto**, Network Monitor chiama la funzione [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="df0ce-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="df0ce-143">Quando gli esperti analizzano i frame richiesti e individuano un problema, usano [**ExpertSubmitEvent**](expertsubmitevent.md) per inviare un evento che contiene informazioni sul problema.</span><span class="sxs-lookup"><span data-stu-id="df0ce-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="df0ce-144">Network Monitor distribuisce l'evento al Visualizzatore eventi standard (condiviso) o (se l'esperto esegue la registrazione) a una Visualizzatore eventi privata.</span><span class="sxs-lookup"><span data-stu-id="df0ce-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



