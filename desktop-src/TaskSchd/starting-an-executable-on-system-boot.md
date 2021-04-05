---
title: Avvio di un eseguibile all'avvio del sistema
description: La scrittura di un'attività che avvia un eseguibile quando un sistema viene avviato viene eseguita definendo un trigger di avvio e un'azione eseguibile.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, trigger di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712577"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="511dc-104">Avvio di un eseguibile all'avvio del sistema</span><span class="sxs-lookup"><span data-stu-id="511dc-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="511dc-105">La scrittura di un'attività che avvia un eseguibile quando un sistema viene avviato viene eseguita definendo un trigger di avvio e un'azione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="511dc-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="511dc-106">Trigger di avvio</span><span class="sxs-lookup"><span data-stu-id="511dc-106">Boot Trigger</span></span>

<span data-ttu-id="511dc-107">I trigger di avvio vengono attivati dal limite iniziale, ma non avviano l'eseguibile fino a quando il sistema non viene avviato.</span><span class="sxs-lookup"><span data-stu-id="511dc-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="511dc-108">È anche possibile specificare un tempo di ritardo nel trigger di avvio che specifica la quantità di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="511dc-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="511dc-109">Questa impostazione è definita dalla proprietà [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) nell'interfaccia [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (oggetto [**BootTrigger**](boottrigger.md) per lo scripting).</span><span class="sxs-lookup"><span data-stu-id="511dc-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="511dc-110">Esempi di trigger di avvio</span><span class="sxs-lookup"><span data-stu-id="511dc-110">Boot Trigger Examples</span></span>

<span data-ttu-id="511dc-111">Gli esempi seguenti avviano il blocco note dopo l'avvio del sistema:</span><span class="sxs-lookup"><span data-stu-id="511dc-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="511dc-112">Esempio di trigger di avvio (scripting)</span><span class="sxs-lookup"><span data-stu-id="511dc-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="511dc-113">Esempio di trigger di avvio (C++)</span><span class="sxs-lookup"><span data-stu-id="511dc-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="511dc-114">Esempio di trigger di avvio (XML)</span><span class="sxs-lookup"><span data-stu-id="511dc-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="511dc-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="511dc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="511dc-116">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="511dc-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




