---
title: Esempio di creazione di un'attività con NewWorkItem
description: Quando si crea un'attività, si utilizzeranno due interfacce Utilità di pianificazione ITaskScheduler e ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- creazione di elementi di lavoro Utilità di pianificazione
- elementi di lavoro Utilità di pianificazione, creazione di attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338390"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="28837-105">Esempio di creazione di un'attività con NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="28837-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="28837-106">Quando si crea un'attività, si useranno due interfacce di Utilità di pianificazione: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) e [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="28837-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="28837-107">È necessario specificare un nome univoco per l'attività, l'identificatore di classe dell'oggetto attività e l'identificatore di interfaccia di **ITask**.</span><span class="sxs-lookup"><span data-stu-id="28837-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="28837-108">L'identificatore di classe e l'identificatore di interfaccia vengono mostrati nell'esempio di codice riportato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="28837-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="28837-109">È anche possibile creare un'attività chiamando [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span><span class="sxs-lookup"><span data-stu-id="28837-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="28837-110">Quando si esegue questa route, è responsabilità della creazione di un'istanza dell'oggetto **attività** , che supporta l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , quindi aggiungere l'attività con il nome fornito.</span><span class="sxs-lookup"><span data-stu-id="28837-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="28837-111">Per impostazione predefinita, solo un membro del gruppo Administrators, Backup Operators o Server Operators può creare attività in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="28837-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="28837-112">Un membro del gruppo Administrators può modificare il descrittore di sicurezza della \\ cartella attività di Windows per consentire ad altri di creare attività.</span><span class="sxs-lookup"><span data-stu-id="28837-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="28837-113">Il nome fornito per l'attività deve essere univoco all'interno della cartella attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="28837-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="28837-114">Se un'attività con lo stesso nome esiste già, [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) restituisce il \_ file degli errori \_ .</span><span class="sxs-lookup"><span data-stu-id="28837-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="28837-115">Se si ottiene questo valore restituito, è necessario specificare un nome diverso e tentare di creare nuovamente l'attività.</span><span class="sxs-lookup"><span data-stu-id="28837-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="28837-116">Nella procedura seguente viene descritto come creare una nuova attività elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="28837-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="28837-117">**Per creare una nuova attività elemento di lavoro**</span><span class="sxs-lookup"><span data-stu-id="28837-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="28837-118">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="28837-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="28837-119">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="28837-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="28837-120">Chiamare [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) per creare una nuova attività.</span><span class="sxs-lookup"><span data-stu-id="28837-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="28837-121">Questo metodo restituisce un puntatore a un'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="28837-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="28837-122">Salvare la nuova attività su disco chiamando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="28837-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="28837-123">L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia **ITask** .</span><span class="sxs-lookup"><span data-stu-id="28837-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="28837-124">Chiamare **ITask:: Release** per rilasciare tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="28837-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="28837-125">Si noti che la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="28837-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="28837-126">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="28837-126">For a code example of</span></span>  | <span data-ttu-id="28837-127">Vedere</span><span class="sxs-lookup"><span data-stu-id="28837-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28837-128">Creazione di una singola attività</span><span class="sxs-lookup"><span data-stu-id="28837-128">Creating a single task</span></span> | [<span data-ttu-id="28837-129">Esempio di codice C/C++: creazione di un'attività con NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="28837-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="28837-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28837-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28837-131">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="28837-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 