---
description: L'applicazione è divisa in due programmi. Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modello di broker amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882642"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="48932-104">Modello di broker amministratore</span><span class="sxs-lookup"><span data-stu-id="48932-104">Administrator Broker Model</span></span>

<span data-ttu-id="48932-105">Nel modello di broker di amministrazione, l'applicazione è divisa in due programmi.</span><span class="sxs-lookup"><span data-stu-id="48932-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="48932-106">Uno dei programmi viene eseguito come utente standard e l'altro viene eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="48932-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="48932-107">Utilizzando un manifesto dell'applicazione, contrassegnare il programma utente standard con un **requestedExecutionLevel** di **asInvoker** e contrassegnare il programma amministrativo con **requestedExecutionLevel** **requireAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="48932-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="48932-108">Un utente avvia prima il programma utente standard.</span><span class="sxs-lookup"><span data-stu-id="48932-108">A user launches the standard user program first.</span></span> <span data-ttu-id="48932-109">Quando l'utente tenta di eseguire un'operazione che richiede un token di accesso amministratore completo, il programma utente standard chiama la funzione [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) per avviare il programma amministrativo.</span><span class="sxs-lookup"><span data-stu-id="48932-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="48932-110">La funzione **ShellExecute** richiede l'approvazione dell'utente prima di eseguire l'applicazione con il token di accesso amministratore completo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="48932-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="48932-111">Il programma amministrativo può quindi eseguire attività che richiedono privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="48932-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="48932-112">Il programma di amministrazione non è completamente isolato dal programma utente standard.</span><span class="sxs-lookup"><span data-stu-id="48932-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="48932-113">Il programma amministrativo può abilitare la comunicazione interprocesso con il programma utente standard.</span><span class="sxs-lookup"><span data-stu-id="48932-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="48932-114">Tuttavia, tale comunicazione è limitata dai criteri di integrità obbligatori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="48932-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="48932-115">Per informazioni sulle considerazioni sull'integrità obbligatoria, vedere [progettazione di applicazioni per l'esecuzione a un livello di integrità basso](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="48932-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="48932-116">Di seguito sono riportati gli utilizzi possibili per il modello di broker amministratore:</span><span class="sxs-lookup"><span data-stu-id="48932-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="48932-117">Sviluppo di procedure guidate.</span><span class="sxs-lookup"><span data-stu-id="48932-117">Developing wizards.</span></span> <span data-ttu-id="48932-118">Quando una procedura guidata hardware determina che un driver richiesto non è installato nel computer o che si trova nella posizione approvata dell'organizzazione, chiama un'applicazione con privilegi elevati con la possibilità di spostare un driver nell'archivio del computer.</span><span class="sxs-lookup"><span data-stu-id="48932-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="48932-119">Autorun.exe la chiamata di Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="48932-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="48932-120">Quando un utente esegue software da un CD, Autorun.exe, che viene eseguito come utente standard, avvia Setup.exe, che viene eseguito come amministratore, per installare il software nel computer.</span><span class="sxs-lookup"><span data-stu-id="48932-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="48932-121">Di seguito sono riportati gli svantaggi dell'utilizzo del modello di broker Administrator:</span><span class="sxs-lookup"><span data-stu-id="48932-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="48932-122">Le transizioni dall'applicazione all'applicazione possono confondere l'utente.</span><span class="sxs-lookup"><span data-stu-id="48932-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="48932-123">Può essere difficile informare l'utente del motivo per cui viene visualizzata una nuova applicazione sul monitor.</span><span class="sxs-lookup"><span data-stu-id="48932-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="48932-124">Può essere difficile passare le informazioni sullo stato tra le due applicazioni.</span><span class="sxs-lookup"><span data-stu-id="48932-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="48932-125">Non è ad esempio possibile usare questo modello per passare le informazioni sullo stato tra un pannello di controllo utente standard (CPL) e la relativa controparte amministratore semplicemente per consentire allo stesso CPL di avere funzionalità utente amministrative e standard.</span><span class="sxs-lookup"><span data-stu-id="48932-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="48932-126">L'utente standard CPL avrebbe dovuto archiviare lo stato in un punto qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="48932-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="48932-127">Quando si suddivide la funzionalità tra due programmi, può essere presente una grande quantità di codice replicato.</span><span class="sxs-lookup"><span data-stu-id="48932-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48932-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48932-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48932-129">Sviluppo di applicazioni che richiedono privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="48932-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="48932-130">Modello a oggetti COM dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="48932-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="48932-131">Modello di servizio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="48932-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="48932-132">Modello di attività con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="48932-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
