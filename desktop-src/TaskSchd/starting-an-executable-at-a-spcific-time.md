---
title: Avvio di un eseguibile in un momento specifico
description: La scrittura di un'attività che avvia un eseguibile in un momento specifico viene eseguita definendo un trigger di ora e un'azione eseguibile.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, Trigger Time
- Esempi di Utilità di pianificazione Utilità di pianificazione, avvio di un eseguibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856501"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="11405-105">Avvio di un eseguibile in un momento specifico</span><span class="sxs-lookup"><span data-stu-id="11405-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="11405-106">La scrittura di un'attività che avvia un eseguibile in un momento specifico viene eseguita definendo un trigger di ora e un'azione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="11405-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="11405-107">Limite iniziale</span><span class="sxs-lookup"><span data-stu-id="11405-107">Start Boundary</span></span>

<span data-ttu-id="11405-108">È importante notare che un trigger di ora è diverso dagli altri trigger basati sul tempo in quanto viene generato quando il trigger viene attivato dal limite iniziale.</span><span class="sxs-lookup"><span data-stu-id="11405-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="11405-109">Altri trigger basati sul tempo vengono attivati dal limite iniziale, ma non iniziano a eseguire le azioni, in questo caso avviando un eseguibile, fino a quando non viene raggiunta una data pianificata.</span><span class="sxs-lookup"><span data-stu-id="11405-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="11405-110">Esempi di trigger di ora</span><span class="sxs-lookup"><span data-stu-id="11405-110">Time Trigger Examples</span></span>

<span data-ttu-id="11405-111">Gli esempi seguenti avviano il blocco note 30 secondi dopo l'attivazione dell'attività:</span><span class="sxs-lookup"><span data-stu-id="11405-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="11405-112">Esempio di trigger time (C++)</span><span class="sxs-lookup"><span data-stu-id="11405-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="11405-113">Esempio di trigger di ora (scripting)</span><span class="sxs-lookup"><span data-stu-id="11405-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="11405-114">Esempio di trigger time (XML)</span><span class="sxs-lookup"><span data-stu-id="11405-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="11405-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11405-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11405-116">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="11405-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




