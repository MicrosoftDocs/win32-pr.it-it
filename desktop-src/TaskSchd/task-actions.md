---
title: Azioni attività
description: Gli elementi di lavoro eseguiti da un'attività vengono chiamati azioni. Un'attività può avere una sola azione o un massimo di 32 azioni. Tenere presente che, quando si specificano più azioni, vengono eseguite in modo sequenziale.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- azioni Utilità di pianificazione
- azioni Utilità di pianificazione, descritte
- azioni Utilità di pianificazione, Esegui azione
- azioni Utilità di pianificazione, azione gestore COM
- Esegui azione Utilità di pianificazione
- Utilità di pianificazione azione gestore COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "103722057"
---
# <a name="task-actions"></a><span data-ttu-id="e804c-111">Azioni attività</span><span class="sxs-lookup"><span data-stu-id="e804c-111">Task Actions</span></span>

<span data-ttu-id="e804c-112">Gli elementi di lavoro eseguiti da un'attività vengono chiamati azioni.</span><span class="sxs-lookup"><span data-stu-id="e804c-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="e804c-113">Un'attività può avere una sola azione o un massimo di 32 azioni.</span><span class="sxs-lookup"><span data-stu-id="e804c-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="e804c-114">Tenere presente che, quando si specificano più azioni, vengono eseguite in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="e804c-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="e804c-115">Tipi di azioni</span><span class="sxs-lookup"><span data-stu-id="e804c-115">Types of Actions</span></span>

<span data-ttu-id="e804c-116">Nella seguente tabella di azioni viene descritto il tipo di lavoro o le azioni che possono essere eseguite da un'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="e804c-117">Tipo di azione</span><span class="sxs-lookup"><span data-stu-id="e804c-117">Type of Action</span></span>      | <span data-ttu-id="e804c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e804c-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e804c-119">Azione del comgestore</span><span class="sxs-lookup"><span data-stu-id="e804c-119">ComHandler Action</span></span>   | <span data-ttu-id="e804c-120">Questa azione attiva un gestore COM.</span><span class="sxs-lookup"><span data-stu-id="e804c-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="e804c-121">Azione exec</span><span class="sxs-lookup"><span data-stu-id="e804c-121">Exec Action</span></span>         | <span data-ttu-id="e804c-122">Questa azione esegue un'operazione della riga di comando, ad esempio l'avvio del blocco note.</span><span class="sxs-lookup"><span data-stu-id="e804c-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="e804c-123">Azione di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="e804c-123">E-mail Action</span></span>       | <span data-ttu-id="e804c-124">Questa azione Invia un messaggio di posta elettronica quando viene attivata un'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="e804c-125">Mostra azione messaggio</span><span class="sxs-lookup"><span data-stu-id="e804c-125">Show Message Action</span></span> | <span data-ttu-id="e804c-126">Questa azione Visualizza una finestra di messaggio con un messaggio e un titolo specificati.</span><span class="sxs-lookup"><span data-stu-id="e804c-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="e804c-127">Specifica di azioni</span><span class="sxs-lookup"><span data-stu-id="e804c-127">Specifying Actions</span></span>

<span data-ttu-id="e804c-128">Le azioni di un'attività vengono specificate quando l'attività viene definita e archiviata in una raccolta di azioni usate dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e804c-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="e804c-129">La tabella seguente elenca i collegamenti agli argomenti di riferimento per le API e gli elementi XML associati alle azioni.</span><span class="sxs-lookup"><span data-stu-id="e804c-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="e804c-130">Per ulteriori informazioni ed esempi su come utilizzare le interfacce Utilità di pianificazione, gli oggetti di script e il codice XML, vedere [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="e804c-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="e804c-131">API di interfaccia per lo sviluppo in C++</span><span class="sxs-lookup"><span data-stu-id="e804c-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="e804c-132">API</span><span class="sxs-lookup"><span data-stu-id="e804c-132">API</span></span>                                                                    | <span data-ttu-id="e804c-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e804c-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e804c-134">**Proprietà Actions di ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="e804c-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="e804c-135">Ottiene o imposta le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="e804c-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="e804c-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="e804c-137">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="e804c-138">**IComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="e804c-139">Rappresenta un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="e804c-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="e804c-140">**IExecAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="e804c-141">Rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e804c-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="e804c-142">**IEmailAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="e804c-143">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="e804c-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="e804c-144">**IShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="e804c-145">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e804c-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="e804c-146">API di oggetti di scripting per lo sviluppo di script</span><span class="sxs-lookup"><span data-stu-id="e804c-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="e804c-147">API</span><span class="sxs-lookup"><span data-stu-id="e804c-147">API</span></span>                                                      | <span data-ttu-id="e804c-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e804c-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e804c-149">**TaskDefinition. Actions**</span><span class="sxs-lookup"><span data-stu-id="e804c-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="e804c-150">Ottiene o imposta le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="e804c-151">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="e804c-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="e804c-152">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="e804c-153">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="e804c-154">Rappresenta un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="e804c-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="e804c-155">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="e804c-156">Rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e804c-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="e804c-157">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="e804c-158">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="e804c-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="e804c-159">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="e804c-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="e804c-160">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e804c-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="e804c-161">Elementi XML</span><span class="sxs-lookup"><span data-stu-id="e804c-161">XML Elements</span></span>



| <span data-ttu-id="e804c-162">Elemento</span><span class="sxs-lookup"><span data-stu-id="e804c-162">Element</span></span>                                                                    | <span data-ttu-id="e804c-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e804c-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e804c-164">**Azioni**</span><span class="sxs-lookup"><span data-stu-id="e804c-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="e804c-165">Definisce le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="e804c-166">**Comgestore**</span><span class="sxs-lookup"><span data-stu-id="e804c-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="e804c-167">Rappresenta un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="e804c-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="e804c-168">**Exec**</span><span class="sxs-lookup"><span data-stu-id="e804c-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="e804c-169">Rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e804c-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="e804c-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="e804c-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="e804c-171">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="e804c-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="e804c-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="e804c-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="e804c-173">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e804c-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="e804c-174">Utilizzo di variabili nelle proprietà dell'azione</span><span class="sxs-lookup"><span data-stu-id="e804c-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="e804c-175">Alcune proprietà di azione di tipo **BSTR** possono contenere variabili $ (Arg0), $ (arg1),..., $ (Arg32) nei relativi valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="e804c-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="e804c-176">Queste variabili vengono sostituite con i valori specificati nel parametro *params* dei metodi [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) e [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) oppure sono contenuti nel trigger di evento per l'attività.</span><span class="sxs-lookup"><span data-stu-id="e804c-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="e804c-177">Nella tabella seguente sono elencate le proprietà dell'azione che possono usare variabili nei valori stringa.</span><span class="sxs-lookup"><span data-stu-id="e804c-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e804c-178">Azione</span><span class="sxs-lookup"><span data-stu-id="e804c-178">Action</span></span></th>
<th><span data-ttu-id="e804c-179">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e804c-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e804c-180">Azione gestore COM</span><span class="sxs-lookup"><span data-stu-id="e804c-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="e804c-181">C++:</span><span class="sxs-lookup"><span data-stu-id="e804c-181">C++:</span></span>
<ul>
<li><span data-ttu-id="e804c-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Proprietà ClassID di IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Proprietà Data di IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="e804c-184">Scripting:</span><span class="sxs-lookup"><span data-stu-id="e804c-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="e804c-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction. ClassID</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="e804c-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction. Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e804c-187">Azione di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="e804c-187">Email Action</span></span></td>
<td><span data-ttu-id="e804c-188">C++:</span><span class="sxs-lookup"><span data-stu-id="e804c-188">C++:</span></span>
<ul>
<li><span data-ttu-id="e804c-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Proprietà Body di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Proprietà server di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Proprietà Subject di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Alla proprietà di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Proprietà CC di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Proprietà Ccn di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Proprietà ReplyTo di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Proprietà from di IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="e804c-197">Scripting:</span><span class="sxs-lookup"><span data-stu-id="e804c-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="e804c-198"><a href="emailaction-body.md"><strong>EmailAction. Body</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="e804c-199"><a href="emailaction-server.md"><strong>EmailAction. Server</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="e804c-200"><a href="emailaction-subject.md"><strong>EmailAction. Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="e804c-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="e804c-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="e804c-203"><a href="emailaction-bcc.md"><strong>EmailAction. Ccn</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="e804c-204"><a href="emailaction-replyto.md"><strong>EmailAction. ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="e804c-205"><a href="emailaction-from.md"><strong>EmailAction. from</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e804c-206">Azione exec</span><span class="sxs-lookup"><span data-stu-id="e804c-206">Exec Action</span></span></td>
<td><span data-ttu-id="e804c-207">C++:</span><span class="sxs-lookup"><span data-stu-id="e804c-207">C++:</span></span>
<ul>
<li><span data-ttu-id="e804c-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Proprietà Arguments di IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Proprietà WorkingDirectory di IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="e804c-210">Scripting:</span><span class="sxs-lookup"><span data-stu-id="e804c-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="e804c-211"><a href="execaction-arguments.md"><strong>ExecAction. Arguments</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="e804c-212"><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e804c-213">Mostra azione messaggio</span><span class="sxs-lookup"><span data-stu-id="e804c-213">Show Message Action</span></span></td>
<td><span data-ttu-id="e804c-214">C++:</span><span class="sxs-lookup"><span data-stu-id="e804c-214">C++:</span></span>
<ul>
<li><span data-ttu-id="e804c-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Proprietà title di IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="e804c-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Proprietà MessageBody di IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="e804c-217">Scripting:</span><span class="sxs-lookup"><span data-stu-id="e804c-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="e804c-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction. title</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="e804c-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></span><span class="sxs-lookup"><span data-stu-id="e804c-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e804c-220">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e804c-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e804c-221">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e804c-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





