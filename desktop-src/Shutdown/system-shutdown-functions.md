---
description: Le funzioni seguenti vengono utilizzate con l'arresto del sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funzioni di arresto del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967608"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="4333b-103">Funzioni di arresto del sistema</span><span class="sxs-lookup"><span data-stu-id="4333b-103">System Shutdown Functions</span></span>

<span data-ttu-id="4333b-104">Le funzioni seguenti vengono utilizzate con l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="4333b-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="4333b-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="4333b-105">Function</span></span>                                                         | <span data-ttu-id="4333b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4333b-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4333b-107">**AbortSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="4333b-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="4333b-108">Arresta un arresto del sistema che è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="4333b-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="4333b-109">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="4333b-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="4333b-110">Disconnette l'utente interattivo.</span><span class="sxs-lookup"><span data-stu-id="4333b-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="4333b-111">**ExitWindowsEx**</span><span class="sxs-lookup"><span data-stu-id="4333b-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="4333b-112">Disconnette l'utente interattivo, arresta il sistema o arresta e riavvia il sistema...</span><span class="sxs-lookup"><span data-stu-id="4333b-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="4333b-113">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="4333b-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="4333b-114">Avvia un arresto e un riavvio del computer specificato e riavvia tutte le applicazioni che sono state registrate per il riavvio.</span><span class="sxs-lookup"><span data-stu-id="4333b-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="4333b-115">**InitiateSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="4333b-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="4333b-116">Avvia un arresto e un riavvio facoltativo del computer specificato.</span><span class="sxs-lookup"><span data-stu-id="4333b-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="4333b-117">**InitiateSystemShutdownEx**</span><span class="sxs-lookup"><span data-stu-id="4333b-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="4333b-118">Avvia un arresto e un riavvio facoltativo del computer specificato e, facoltativamente, registra il motivo dell'arresto.</span><span class="sxs-lookup"><span data-stu-id="4333b-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="4333b-119">**LockWorkStation**</span><span class="sxs-lookup"><span data-stu-id="4333b-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="4333b-120">Blocca la visualizzazione della workstation.</span><span class="sxs-lookup"><span data-stu-id="4333b-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="4333b-121">**ShutdownBlockReasonCreate**</span><span class="sxs-lookup"><span data-stu-id="4333b-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="4333b-122">Indica che il sistema non può essere arrestato e imposta una stringa del motivo da visualizzare all'utente se l'arresto del sistema è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="4333b-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="4333b-123">**ShutdownBlockReasonDestroy**</span><span class="sxs-lookup"><span data-stu-id="4333b-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="4333b-124">Indica che è possibile arrestare il sistema e liberare la stringa del motivo.</span><span class="sxs-lookup"><span data-stu-id="4333b-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="4333b-125">**ShutdownBlockReasonQuery**</span><span class="sxs-lookup"><span data-stu-id="4333b-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="4333b-126">Recupera la stringa del motivo impostata dalla funzione [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="4333b-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 



