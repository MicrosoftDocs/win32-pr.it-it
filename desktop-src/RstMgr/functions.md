---
title: Funzioni di gestione riavvio
description: L'API di gestione riavvio usa le funzioni identificate nella tabella seguente.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Gestione riavvio riavvio gestione, informazioni di riferimento, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855966"
---
# <a name="restart-manager-functions"></a><span data-ttu-id="2d58b-104">Funzioni di gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="2d58b-104">Restart Manager Functions</span></span>

<span data-ttu-id="2d58b-105">L'API di gestione riavvio usa le funzioni identificate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2d58b-105">The Restart Manager API uses the functions identified in the following table.</span></span>



| <span data-ttu-id="2d58b-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="2d58b-106">Function</span></span>                                           | <span data-ttu-id="2d58b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d58b-107">Description</span></span>                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d58b-108">**RmAddFilter**</span><span class="sxs-lookup"><span data-stu-id="2d58b-108">**RmAddFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | <span data-ttu-id="2d58b-109">Modifica le azioni di arresto o riavvio.</span><span class="sxs-lookup"><span data-stu-id="2d58b-109">Modifies shutdown or restart actions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="2d58b-110">**RmStartSession**</span><span class="sxs-lookup"><span data-stu-id="2d58b-110">**RmStartSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | <span data-ttu-id="2d58b-111">Avvia una nuova sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="2d58b-111">Starts a new Restart Manager session.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="2d58b-112">**RmJoinSession**</span><span class="sxs-lookup"><span data-stu-id="2d58b-112">**RmJoinSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | <span data-ttu-id="2d58b-113">Consente di unire il processo di un'applicazione a una sessione di gestione riavvio esistente.</span><span class="sxs-lookup"><span data-stu-id="2d58b-113">Joins the process of an application to an existing Restart Manager session.</span></span>                                                                                                                  |
| [<span data-ttu-id="2d58b-114">**RmEndSession**</span><span class="sxs-lookup"><span data-stu-id="2d58b-114">**RmEndSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | <span data-ttu-id="2d58b-115">Termina la sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="2d58b-115">Ends the Restart Manager session.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="2d58b-116">**RmRegisterResources**</span><span class="sxs-lookup"><span data-stu-id="2d58b-116">**RmRegisterResources**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | <span data-ttu-id="2d58b-117">Registra le risorse, ad esempio i nomi file, i nomi brevi del servizio o le strutture di [**\_ \_ processo univoche RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , in una sessione di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="2d58b-117">Registers resources, such as filenames, service short names, or [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structures, to a Restart Manager session.</span></span>                                   |
| [<span data-ttu-id="2d58b-118">**RmGetList**</span><span class="sxs-lookup"><span data-stu-id="2d58b-118">**RmGetList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | <span data-ttu-id="2d58b-119">Usato dai programmi di installazione per ottenere un elenco di tutte le applicazioni interessate dalle risorse registrate e dal relativo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="2d58b-119">Used by installers to get a list of all applications affected by registered resources and their current status.</span></span>                                                                              |
| [<span data-ttu-id="2d58b-120">**RmGetFilterList**</span><span class="sxs-lookup"><span data-stu-id="2d58b-120">**RmGetFilterList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | <span data-ttu-id="2d58b-121">Esegue una query sullo stato di arresto e riavvio delle modifiche già applicate.</span><span class="sxs-lookup"><span data-stu-id="2d58b-121">Queries the status of shutdown and restart modifications that have already been applied.</span></span>                                                                                                     |
| [<span data-ttu-id="2d58b-122">**RmShutdown**</span><span class="sxs-lookup"><span data-stu-id="2d58b-122">**RmShutdown**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | <span data-ttu-id="2d58b-123">Avvia l'arresto di applicazioni e servizi.</span><span class="sxs-lookup"><span data-stu-id="2d58b-123">Initiates the shut down of applications and services.</span></span>                                                                                                                                        |
| [<span data-ttu-id="2d58b-124">**RmRemoveFilter**</span><span class="sxs-lookup"><span data-stu-id="2d58b-124">**RmRemoveFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | <span data-ttu-id="2d58b-125">Rimuove le modifiche di arresto e riavvio che sono già state applicate.</span><span class="sxs-lookup"><span data-stu-id="2d58b-125">Removes shutdown and restart modifications that have already been applied.</span></span>                                                                                                                   |
| [<span data-ttu-id="2d58b-126">**RmRestart**</span><span class="sxs-lookup"><span data-stu-id="2d58b-126">**RmRestart**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | <span data-ttu-id="2d58b-127">Riavvia le applicazioni e i servizi che sono stati arrestati dalla funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) e che sono stati registrati per il riavvio usando **RegisterApplicationRestart**.</span><span class="sxs-lookup"><span data-stu-id="2d58b-127">Restarts applications and services that have been shut down by the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function and that have been registered for restart using **RegisterApplicationRestart**.</span></span> |
| [<span data-ttu-id="2d58b-128">**RmCancelCurrentTask**</span><span class="sxs-lookup"><span data-stu-id="2d58b-128">**RmCancelCurrentTask**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | <span data-ttu-id="2d58b-129">Annulla la funzione [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) corrente.</span><span class="sxs-lookup"><span data-stu-id="2d58b-129">Cancels the current [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown), or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>                                                            |



 

 

 




