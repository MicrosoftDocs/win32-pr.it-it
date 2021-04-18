---
title: Linee guida per le attività in background in Servizi Desktop remoto
description: Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297989"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a><span data-ttu-id="30a6e-103">Linee guida per le attività in background in Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="30a6e-103">Guidelines for background tasks in Remote Desktop Services</span></span>

<span data-ttu-id="30a6e-104">Attività in background: le attività eseguite quando il ciclo di messaggi di un'applicazione è inattivo, forniscono un meccanismo per gestire le attività con priorità bassa in un ambiente con un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="30a6e-104">Background tasks—tasks performed when an application's message loop is idle—provide a mechanism for handling low-priority tasks in a single-user environment.</span></span> <span data-ttu-id="30a6e-105">In un ambiente di Servizi Desktop remoto, tuttavia, un'attività in background di un utente compete per i cicli della CPU con le attività in primo piano di un altro utente.</span><span class="sxs-lookup"><span data-stu-id="30a6e-105">In a Remote Desktop Services environment, however, one user's background task competes for CPU cycles with another user's foreground tasks.</span></span> <span data-ttu-id="30a6e-106">Quando più utenti eseguono attività in primo piano e in background, le richieste di CPU sono molto più elevate rispetto a quando tutti gli utenti eseguono solo attività in primo piano.</span><span class="sxs-lookup"><span data-stu-id="30a6e-106">When multiple users are running both foreground and background tasks, the CPU demands are much higher than when all users are running only foreground tasks.</span></span> <span data-ttu-id="30a6e-107">Per ottimizzare la disponibilità della CPU per tutti gli utenti, disabilitare le attività in background durante l'esecuzione in un ambiente Servizi Desktop remoto o creare attività in background efficienti che non richiedono un uso intensivo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="30a6e-107">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

<span data-ttu-id="30a6e-108">Per ulteriori informazioni, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="30a6e-108">For more information, see [Detecting the Remote Desktop Services environment](detecting-the-terminal-services-environment.md).</span></span> <span data-ttu-id="30a6e-109">Dopo aver rilevato l'ambiente di Servizi Desktop remoto, è possibile disabilitare o riconfigurare le attività in background per l'applicazione usando lo stesso set di API usato per gestire le attività.</span><span class="sxs-lookup"><span data-stu-id="30a6e-109">After you detect the Remote Desktop Services environment, you can disable or reconfigure background tasks for the application using the same set of APIs that you used to manage the tasks.</span></span>

 

 




