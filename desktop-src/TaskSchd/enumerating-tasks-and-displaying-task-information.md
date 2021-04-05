---
title: Enumerazione delle attività e visualizzazione delle informazioni sulle attività
description: La visualizzazione delle informazioni su un'attività, ad esempio il nome dell'attività, lo stato o l'ultima esecuzione dell'attività, viene eseguita tramite l'enumerazione delle attività in esecuzione o delle attività in una cartella di attività e la visualizzazione delle informazioni desiderate.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Enumerazione delle attività Utilità di pianificazione
- Esempi di Utilità di pianificazione Utilità di pianificazione, enumerazione delle attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707279"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="c5f9f-105">Enumerazione delle attività e visualizzazione delle informazioni sulle attività</span><span class="sxs-lookup"><span data-stu-id="c5f9f-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="c5f9f-106">La visualizzazione delle informazioni su un'attività, ad esempio il nome dell'attività, lo stato o l'ultima esecuzione dell'attività, viene eseguita tramite l'enumerazione delle attività in esecuzione o delle attività in una cartella di attività e la visualizzazione delle informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="c5f9f-107">Accesso alle proprietà delle attività registrate</span><span class="sxs-lookup"><span data-stu-id="c5f9f-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="c5f9f-108">Per visualizzare il valore della proprietà di un'attività registrata, è necessario connettersi al servizio Utilità di pianificazione e quindi ottenere un'istanza della cartella attività che contiene le attività per le quali si desiderano informazioni.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="c5f9f-109">Si otterrà quindi una raccolta di tutte le attività registrate nella cartella delle attività.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="c5f9f-110">È quindi possibile enumerare ogni attività registrata e ottenere e visualizzare un valore di proprietà per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="c5f9f-111">Accesso alle proprietà delle attività in esecuzione</span><span class="sxs-lookup"><span data-stu-id="c5f9f-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="c5f9f-112">Per visualizzare il valore della proprietà di un'attività in esecuzione, è necessario connettersi al servizio Utilità di pianificazione e quindi ottenere una raccolta di tutte le attività in esecuzione (incluse o escluse le attività nascoste).</span><span class="sxs-lookup"><span data-stu-id="c5f9f-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="c5f9f-113">È quindi possibile enumerare ogni attività in esecuzione e ottenere e visualizzare un valore di proprietà per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="c5f9f-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="c5f9f-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="c5f9f-114">Example</span></span>

<span data-ttu-id="c5f9f-115">Negli esempi seguenti vengono enumerate le attività e vengono visualizzati il nome e lo stato delle attività:</span><span class="sxs-lookup"><span data-stu-id="c5f9f-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="c5f9f-116">Visualizzazione di nomi e Stati delle attività (scripting)</span><span class="sxs-lookup"><span data-stu-id="c5f9f-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="c5f9f-117">Visualizzazione di nomi e stato delle attività (C++)</span><span class="sxs-lookup"><span data-stu-id="c5f9f-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="c5f9f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5f9f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f9f-119">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c5f9f-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




