---
title: Annullamento dell'operazione corrente di gestione riavvio
description: Quando un'azione utente indirizza il programma di installazione per eseguire un'azione diversa, è possibile usare il metodo seguente per annullare l'operazione corrente di gestione riavvio.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714659"
---
# <a name="canceling-the-current-restart-manager-operation"></a><span data-ttu-id="16d31-103">Annullamento dell'operazione corrente di gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="16d31-103">Canceling the Current Restart Manager Operation</span></span>

<span data-ttu-id="16d31-104">Quando un'azione utente indirizza il programma di installazione per eseguire un'azione diversa, è possibile usare il metodo seguente per annullare l'operazione corrente di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="16d31-104">When a user action directs the installer to perform a different action, the following method can be used to cancel the current Restart Manager operation.</span></span>

<span data-ttu-id="16d31-105">**Per annullare l'operazione corrente di gestione riavvio**</span><span class="sxs-lookup"><span data-stu-id="16d31-105">**To cancel the current Restart Manager operation**</span></span>

-   <span data-ttu-id="16d31-106">Il programma di installazione può chiamare la funzione [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) da un altro thread per annullare l'operazione corrente di [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .</span><span class="sxs-lookup"><span data-stu-id="16d31-106">The installer can call the [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) function from another thread to cancel the current [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) operation.</span></span> <span data-ttu-id="16d31-107">È possibile che la gestione riavvio annulli l'operazione a seconda della misura in cui l'operazione è stata completata quando viene chiamata la funzione **RMCancelCurrentTask** .</span><span class="sxs-lookup"><span data-stu-id="16d31-107">The Restart Manager may cancel the operation depending on the extent to which the operation has completed when the **RMCancelCurrentTask** function is called.</span></span>

 

 




