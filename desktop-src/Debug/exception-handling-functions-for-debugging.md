---
description: Quando si verifica un'eccezione in un processo di cui è in corso il debug, il sistema invia una notifica al debugger passandovi l'eccezione. Questa operazione è nota come notifica first-chance. Il sistema sospende quindi tutti i thread nel processo di cui è in corso il debug.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funzioni di gestione delle eccezioni per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877161"
---
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="b5b33-105">Funzioni di gestione delle eccezioni per il debug</span><span class="sxs-lookup"><span data-stu-id="b5b33-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="b5b33-106">Quando si verifica un'eccezione in un processo di cui è in corso il debug, il sistema invia una notifica al debugger passandovi l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="b5b33-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="b5b33-107">Questa operazione è nota come *notifica first-chance*.</span><span class="sxs-lookup"><span data-stu-id="b5b33-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="b5b33-108">Il sistema sospende quindi tutti i thread nel processo di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="b5b33-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="b5b33-109">Se il debugger non gestisce l'eccezione, il sistema tenta di individuare un gestore di eccezioni appropriato.</span><span class="sxs-lookup"><span data-stu-id="b5b33-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="b5b33-110">Se il sistema non è in grado di individuare un oggetto appropriato, il sistema informa nuovamente il debugger che si è verificata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="b5b33-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="b5b33-111">Questo è noto come *notifica dell'ultima opportunità*.</span><span class="sxs-lookup"><span data-stu-id="b5b33-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="b5b33-112">Se il debugger non gestisce l'eccezione dopo la notifica dell'ultima probabilità, il sistema termina il processo di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="b5b33-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="b5b33-113">Per ulteriori informazioni, vedere [gestione delle eccezioni del debugger](debugger-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b5b33-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



