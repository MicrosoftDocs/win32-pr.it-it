---
title: Esempio di recupero di una pagina attività
description: Per recuperare una pagina di attività, è necessario chiamare ITask QueryInterface per recuperare l'interfaccia IProvideTaskPage, quindi chiamare IProvideTaskPage GetPage. Il Metodo GetPage restituisce un handle per la pagina, che può quindi essere usato per visualizzare la pagina richiesta.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recupero della pagina di attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046911"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="dda02-105">Esempio di recupero di una pagina attività</span><span class="sxs-lookup"><span data-stu-id="dda02-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="dda02-106">Per recuperare una pagina di attività, è necessario chiamare **ITask:: QueryInterface** per recuperare l'interfaccia [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) , quindi chiamare [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span><span class="sxs-lookup"><span data-stu-id="dda02-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="dda02-107">Il metodo **GetPage** restituisce un handle per la pagina, che può quindi essere usato per visualizzare la pagina richiesta.</span><span class="sxs-lookup"><span data-stu-id="dda02-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="dda02-108">Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="dda02-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="dda02-109">Nella procedura riportata di seguito viene descritto come creare un nuovo trigger.</span><span class="sxs-lookup"><span data-stu-id="dda02-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="dda02-110">**Per creare un nuovo trigger**</span><span class="sxs-lookup"><span data-stu-id="dda02-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="dda02-111">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="dda02-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="dda02-112">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dda02-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="dda02-113">Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività.</span><span class="sxs-lookup"><span data-stu-id="dda02-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="dda02-114">Si noti che questo esempio Mostra come ottenere l'attività di test.</span><span class="sxs-lookup"><span data-stu-id="dda02-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="dda02-115">Chiamare **ITask:: QueryInterface** per recuperare l'interfaccia [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) per recuperare la pagina.</span><span class="sxs-lookup"><span data-stu-id="dda02-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="dda02-116">Usando l'handle di pagina restituito, visualizzare la pagina.</span><span class="sxs-lookup"><span data-stu-id="dda02-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="dda02-117">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="dda02-117">For a code example of</span></span>                                   | <span data-ttu-id="dda02-118">Vedere</span><span class="sxs-lookup"><span data-stu-id="dda02-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="dda02-119">Recupero e visualizzazione della pagina attività di un'attività nota</span><span class="sxs-lookup"><span data-stu-id="dda02-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="dda02-120">Recupero di una pagina di attività</span><span class="sxs-lookup"><span data-stu-id="dda02-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="dda02-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dda02-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dda02-122">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="dda02-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 