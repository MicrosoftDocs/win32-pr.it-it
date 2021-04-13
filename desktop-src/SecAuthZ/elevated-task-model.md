---
description: Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modello di attività con privilegi elevati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348931"
---
# <a name="elevated-task-model"></a><span data-ttu-id="1cac2-103">Modello di attività con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="1cac2-103">Elevated Task Model</span></span>

<span data-ttu-id="1cac2-104">Nel modello di attività con privilegi elevati, un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore avviando un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="1cac2-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="1cac2-105">**Windows Server 2003 e Windows XP:** Il modello di attività con privilegi elevati non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1cac2-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="1cac2-106">Le attività non utilizzano il numero di risorse di sistema dei servizi e le attività si chiudono automaticamente al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1cac2-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="1cac2-107">È consigliabile utilizzare questo modello anziché il [modello di servizio del sistema operativo](operating-system-service-model.md) a meno che non sia necessaria la compatibilità con le versioni precedenti dei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="1cac2-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="1cac2-108">Per utilizzare un'attività per eseguire operazioni con privilegi per un'applicazione utente standard, è necessario che siano soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cac2-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="1cac2-109">L'attività deve essere impostata per l'esecuzione come **System**.</span><span class="sxs-lookup"><span data-stu-id="1cac2-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="1cac2-110">Il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) associato all'attività deve essere configurato in modo da consentire agli utenti standard di avviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="1cac2-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="1cac2-111">Il servizio Utilità di pianificazione deve essere in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1cac2-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="1cac2-112">Per informazioni su come creare e avviare le attività, vedere [utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page).</span><span class="sxs-lookup"><span data-stu-id="1cac2-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cac2-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1cac2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cac2-114">Sviluppo di applicazioni che richiedono privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="1cac2-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="1cac2-115">Modello di broker amministratore</span><span class="sxs-lookup"><span data-stu-id="1cac2-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="1cac2-116">Modello a oggetti COM dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="1cac2-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="1cac2-117">Modello di servizio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1cac2-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
