---
title: Esempio di attività di enumerazione
description: Per enumerare le attività, è necessario chiamare l'enumerazione ITaskScheduler per creare un oggetto di enumerazione. Utilizzare quindi l'interfaccia IEnumWorkItems dell'oggetto enumerazione per enumerare le attività nella cartella delle attività pianificate.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300204"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="3e0e6-104">Esempio di attività di enumerazione</span><span class="sxs-lookup"><span data-stu-id="3e0e6-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="3e0e6-105">Per enumerare le attività, è necessario chiamare [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) per creare un [*oggetto di enumerazione*](e.md).</span><span class="sxs-lookup"><span data-stu-id="3e0e6-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="3e0e6-106">Utilizzare quindi l'interfaccia [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) dell'oggetto enumerazione per enumerare le attività nella cartella delle attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="3e0e6-107">Nella procedura riportata di seguito viene descritto come enumerare le attività nella cartella delle attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="3e0e6-108">**Per enumerare le attività nella cartella delle attività pianificate**</span><span class="sxs-lookup"><span data-stu-id="3e0e6-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="3e0e6-109">Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="3e0e6-110">In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="3e0e6-111">Chiamare [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) per ottenere un oggetto di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="3e0e6-112">Chiamare [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) per recuperare le attività.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="3e0e6-113">In questo esempio si tenta di recuperare cinque attività a ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="3e0e6-114">Elabora le attività restituite.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-114">Process the tasks returned.</span></span> <span data-ttu-id="3e0e6-115">In questo esempio il nome di ogni attività viene semplicemente stampato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="3e0e6-116">Rilasciare le risorse.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-116">Release resources.</span></span> <span data-ttu-id="3e0e6-117">Chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria usata per i nomi.</span><span class="sxs-lookup"><span data-stu-id="3e0e6-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="3e0e6-118">Per un esempio di codice di</span><span class="sxs-lookup"><span data-stu-id="3e0e6-118">For a code example of</span></span>                                                         | <span data-ttu-id="3e0e6-119">Vedere</span><span class="sxs-lookup"><span data-stu-id="3e0e6-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3e0e6-120">Enumerazione di tutte le attività nella cartella delle attività pianificate del computer locale</span><span class="sxs-lookup"><span data-stu-id="3e0e6-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="3e0e6-121">Esempio di codice C/C++: enumerazione delle attività</span><span class="sxs-lookup"><span data-stu-id="3e0e6-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="3e0e6-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e0e6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e0e6-123">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="3e0e6-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 