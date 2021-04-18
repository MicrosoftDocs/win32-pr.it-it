---
description: Per l'utente, il vantaggio del multitasking è la possibilità di aprire e utilizzare più applicazioni nello stesso momento. Un utente, ad esempio, può modificare un file con un'applicazione mentre un'altra applicazione sta ricalcolando un foglio di calcolo.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Vantaggi del multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312003"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="9e581-104">Vantaggi del multitasking</span><span class="sxs-lookup"><span data-stu-id="9e581-104">Advantages of Multitasking</span></span>

<span data-ttu-id="9e581-105">Per l'utente, il vantaggio del multitasking è la possibilità di aprire e utilizzare più applicazioni nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="9e581-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="9e581-106">Un utente, ad esempio, può modificare un file con un'applicazione mentre un'altra applicazione sta ricalcolando un foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="9e581-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="9e581-107">Per lo sviluppatore di applicazioni, il vantaggio del multitasking è la possibilità di creare applicazioni che usano più processi e di creare processi che usano più di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e581-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="9e581-108">Un processo può ad esempio avere un thread dell'interfaccia utente che gestisce le interazioni con l'utente (input da tastiera e mouse) e i thread di lavoro che eseguono altre attività mentre il thread dell'interfaccia utente attende l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9e581-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="9e581-109">Se si assegna una priorità più elevata al thread dell'interfaccia utente, l'applicazione sarà più reattiva all'utente, mentre i thread di lavoro utilizzeranno il processore in modo efficiente durante i periodi in cui non è presente alcun input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9e581-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 



