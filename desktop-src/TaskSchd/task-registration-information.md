---
title: Informazioni di registrazione delle attività
description: Le informazioni di registrazione consentono di identificare un'attività in diversi modi. Ad esempio, un'attività può essere identificata dall'autore, dal modo in cui è stata creata (definita origine attività) e dalla data di registrazione.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- informazioni di registrazione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328308"
---
# <a name="task-registration-information"></a><span data-ttu-id="b9462-105">Informazioni di registrazione delle attività</span><span class="sxs-lookup"><span data-stu-id="b9462-105">Task Registration Information</span></span>

<span data-ttu-id="b9462-106">Le informazioni di registrazione consentono di identificare un'attività in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="b9462-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="b9462-107">Ad esempio, un'attività può essere identificata dall'autore, dal modo in cui è stata creata (definita origine attività) e dalla data di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b9462-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="b9462-108">Uso delle informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="b9462-108">Using Registration Information</span></span>

<span data-ttu-id="b9462-109">Le informazioni di registrazione vengono in genere specificate quando l'attività viene creata e quindi utilizzata nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9462-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="b9462-110">Visualizzato dall'interfaccia utente di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b9462-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="b9462-111">Ottiene o imposta tramite script o applicazioni C++.</span><span class="sxs-lookup"><span data-stu-id="b9462-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="b9462-112">In un ambiente aziendale, usato come criterio di ricerca durante l'enumerazione di tutte le attività registrate.</span><span class="sxs-lookup"><span data-stu-id="b9462-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="b9462-113">Tipi di informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="b9462-113">Types of Registration Information</span></span>

<span data-ttu-id="b9462-114">Le informazioni di registrazione delle attività sono definite dalle proprietà dell'oggetto [**RegistrationInfo**](registrationinfo.md) per le applicazioni di scripting, dalle proprietà dell'interfaccia [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) per le applicazioni C++ e dagli elementi figlio dell' [**elemento RegistrationInfo (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) per la lettura o la scrittura di XML.</span><span class="sxs-lookup"><span data-stu-id="b9462-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="b9462-115">Queste proprietà consentono di accedere ai tipi di informazioni di registrazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9462-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="b9462-116">Autore attività</span><span class="sxs-lookup"><span data-stu-id="b9462-116">Task Author</span></span>

    <span data-ttu-id="b9462-117">Utilità di pianificazione imposta l'autore dell'attività al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="b9462-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="b9462-118">Data di registrazione attività</span><span class="sxs-lookup"><span data-stu-id="b9462-118">Task Registration Date</span></span>

    <span data-ttu-id="b9462-119">Utilità di pianificazione imposta questa data quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="b9462-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="b9462-120">Descrizione dell'attività</span><span class="sxs-lookup"><span data-stu-id="b9462-120">Task Description</span></span>

    <span data-ttu-id="b9462-121">Descrizione definita dall'utente che può includere i trigger usati per avviare l'attività o le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="b9462-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="b9462-122">Documentazione delle attività</span><span class="sxs-lookup"><span data-stu-id="b9462-122">Task Documentation</span></span>

    <span data-ttu-id="b9462-123">Documentazione fornita dall'utente necessaria per l'attività.</span><span class="sxs-lookup"><span data-stu-id="b9462-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="b9462-124">Descrittore di sicurezza delle attività</span><span class="sxs-lookup"><span data-stu-id="b9462-124">Task Security Descriptor</span></span>

    <span data-ttu-id="b9462-125">Descrittore di sicurezza fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b9462-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="b9462-126">Origine attività</span><span class="sxs-lookup"><span data-stu-id="b9462-126">Task Source</span></span>

    <span data-ttu-id="b9462-127">Informazioni fornite dall'utente che descrivono la posizione di origine dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b9462-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="b9462-128">Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.</span><span class="sxs-lookup"><span data-stu-id="b9462-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="b9462-129">URI attività</span><span class="sxs-lookup"><span data-stu-id="b9462-129">Task URI</span></span>

    <span data-ttu-id="b9462-130">URI (Uniform Resource Identifier) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="b9462-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="b9462-131">Versione attività</span><span class="sxs-lookup"><span data-stu-id="b9462-131">Task Version</span></span>

    <span data-ttu-id="b9462-132">Informazioni fornite dall'utente utilizzate quando esistono più versioni di un'attività.</span><span class="sxs-lookup"><span data-stu-id="b9462-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="b9462-133">Testo XML</span><span class="sxs-lookup"><span data-stu-id="b9462-133">XML Text</span></span>

    <span data-ttu-id="b9462-134">Una versione in formato XML delle informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b9462-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="b9462-135">Si noti che è possibile impostare o modificare le informazioni di registrazione direttamente tramite questo XML e le proprietà dell'oggetto e dell'interfaccia appropriate verranno aggiornate di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="b9462-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="b9462-136">Registrazione di attività</span><span class="sxs-lookup"><span data-stu-id="b9462-136">Registering Tasks</span></span>

<span data-ttu-id="b9462-137">Un'attività può essere registrata dopo la creazione delle definizioni di attività e le informazioni di registrazione e i valori delle impostazioni vengono forniti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b9462-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="b9462-138">Un'attività viene registrata usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) per le applicazioni di scripting o il metodo [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) per le applicazioni C++.</span><span class="sxs-lookup"><span data-stu-id="b9462-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="b9462-139">Se si desidera registrare un'attività utilizzando XML per definire l'attività, utilizzare il metodo [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) per le applicazioni di scripting e il metodo [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) per le applicazioni C++.</span><span class="sxs-lookup"><span data-stu-id="b9462-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="b9462-140">Nei metodi indicati in precedenza è possibile specificare il contesto di sicurezza per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b9462-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="b9462-141">È necessario essere un amministratore del sistema per pianificare l'esecuzione dei processi in contesti diversi da quelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b9462-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="b9462-142">Per ulteriori informazioni sui contesti di sicurezza per l'esecuzione di attività, vedere [contesti di sicurezza per l'esecuzione di attività](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b9462-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9462-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9462-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9462-144">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b9462-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="b9462-145">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b9462-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




