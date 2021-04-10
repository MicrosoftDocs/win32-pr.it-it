---
title: Avvio di un eseguibile quando un'attività è registrata
description: La scrittura di un'attività che avvia un eseguibile quando un'attività viene registrata viene eseguita definendo un trigger di registrazione e un'azione eseguibile.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, trigger di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955583"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="3ae2f-104">Avvio di un eseguibile quando un'attività è registrata</span><span class="sxs-lookup"><span data-stu-id="3ae2f-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="3ae2f-105">La scrittura di un'attività che avvia un eseguibile quando un'attività viene registrata viene eseguita definendo un trigger di registrazione e un'azione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="3ae2f-106">Trigger di registrazione</span><span class="sxs-lookup"><span data-stu-id="3ae2f-106">Registration Trigger</span></span>

<span data-ttu-id="3ae2f-107">I trigger di registrazione avviano un'attività non appena viene registrata.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="3ae2f-108">È anche possibile specificare un ritardo per il trigger di registrazione, che avvia un'attività dopo un periodo di tempo specifico, ovvero il ritardo, dopo la registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="3ae2f-109">Il ritardo viene specificato nella proprietà [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) dell'interfaccia [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) per lo scripting).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="3ae2f-110">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="3ae2f-111">Esempi di trigger di registrazione</span><span class="sxs-lookup"><span data-stu-id="3ae2f-111">Registration Trigger Examples</span></span>

<span data-ttu-id="3ae2f-112">Gli esempi seguenti avviano il blocco note quando un'attività è registrata:</span><span class="sxs-lookup"><span data-stu-id="3ae2f-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="3ae2f-113">Esempio di trigger di registrazione (scripting)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="3ae2f-114">Esempio di trigger di registrazione (C++)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="3ae2f-115">Esempio di trigger di registrazione (XML)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="3ae2f-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ae2f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ae2f-117">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3ae2f-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




