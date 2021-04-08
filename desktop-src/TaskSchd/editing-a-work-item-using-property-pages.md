---
title: Modifica di un elemento di lavoro utilizzando le pagine delle proprietà
description: È possibile modificare le proprietà di un elemento di lavoro usando l'interfaccia utente grafica fornita dal servizio Utilità di pianificazione.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- modifica di elementi di lavoro Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727986"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="50263-104">Modifica di un elemento di lavoro utilizzando le pagine delle proprietà</span><span class="sxs-lookup"><span data-stu-id="50263-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="50263-105">È possibile modificare le proprietà di un elemento di lavoro usando l'interfaccia utente grafica fornita dal servizio Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="50263-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="50263-106">Attualmente, gli unici elementi di lavoro validi sono attività.</span><span class="sxs-lookup"><span data-stu-id="50263-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="50263-107">Nella procedura riportata di seguito viene descritto come modificare un'attività utilizzando le relative pagine delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="50263-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="50263-108">**Per modificare un'attività usando le pagine delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="50263-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="50263-109">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="50263-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="50263-110">In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="50263-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="50263-111">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="50263-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="50263-112">Si noti che le attività sono attualmente l'unico tipo di elemento di lavoro valido.</span><span class="sxs-lookup"><span data-stu-id="50263-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="50263-113">Chiamare [**IScheduledWorkItem:: EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) per visualizzare le pagine delle proprietà per l'attività.</span><span class="sxs-lookup"><span data-stu-id="50263-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="50263-114">Modificare le proprietà dell'attività in base alle esigenze, quindi fare clic su OK per accettare i nuovi valori e rimuovere le pagine delle proprietà visualizzate.</span><span class="sxs-lookup"><span data-stu-id="50263-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="50263-115">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="50263-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="50263-116">Vedere</span><span class="sxs-lookup"><span data-stu-id="50263-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50263-117">Visualizzazione delle pagine delle proprietà per un'attività nota e consentire a un utente di modificare le proprietà dell'elemento di lavoro</span><span class="sxs-lookup"><span data-stu-id="50263-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="50263-118">Esempio di codice C/C++: modifica di un elemento di lavoro</span><span class="sxs-lookup"><span data-stu-id="50263-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="50263-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50263-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50263-120">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="50263-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 