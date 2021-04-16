---
title: Avvio di un eseguibile quando un utente esegue l'accesso
description: La scrittura di un'attività che avvia un eseguibile quando un utente esegue l'accesso viene eseguita definendo un trigger LOGON e un'azione eseguibile.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, trigger LOGON
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395270"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="18cc9-104">Avvio di un eseguibile quando un utente esegue l'accesso</span><span class="sxs-lookup"><span data-stu-id="18cc9-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="18cc9-105">La scrittura di un'attività che avvia un eseguibile quando un utente esegue l'accesso viene eseguita definendo un trigger LOGON e un'azione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="18cc9-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="18cc9-106">Trigger LOGON</span><span class="sxs-lookup"><span data-stu-id="18cc9-106">Logon Trigger</span></span>

<span data-ttu-id="18cc9-107">I trigger LOGON vengono attivati dal limite iniziale, ma non avviano l'eseguibile fino a quando un utente specificato non esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="18cc9-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="18cc9-108">È possibile specificare il trigger LOGON per l'avvio quando un determinato utente accede specificando l'utente nella proprietà [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) dell'interfaccia [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) per lo scripting).</span><span class="sxs-lookup"><span data-stu-id="18cc9-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="18cc9-109">Esempi di LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="18cc9-109">LogonTrigger Examples</span></span>

<span data-ttu-id="18cc9-110">Gli esempi seguenti avviano il blocco note dopo che un utente ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="18cc9-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="18cc9-111">Esempio di trigger LOGON (scripting)</span><span class="sxs-lookup"><span data-stu-id="18cc9-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="18cc9-112">Esempio di trigger LOGON (C++)</span><span class="sxs-lookup"><span data-stu-id="18cc9-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="18cc9-113">Esempio di trigger LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="18cc9-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="18cc9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18cc9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18cc9-115">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="18cc9-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




