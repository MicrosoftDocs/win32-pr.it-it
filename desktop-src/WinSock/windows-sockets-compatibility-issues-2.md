---
description: Windows Sockets 2 continua a supportare tutte le chiamate di funzione e la semantica di Windows Sockets 1,1, ad eccezione di quelle che si occupano di pseudo-blocco.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problemi di compatibilità di Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226483"
---
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="a0215-103">Problemi di compatibilità di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a0215-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="a0215-104">Windows Sockets 2 continua a supportare tutte le chiamate di funzione e la semantica di Windows Sockets 1,1, ad eccezione di quelle che si occupano di pseudo-blocco.</span><span class="sxs-lookup"><span data-stu-id="a0215-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="a0215-105">Poiché Windows Sockets 2 viene eseguito solo in ambienti a 32 bit e pianificati preventivamente, non è necessario implementare lo pseudo-blocco trovato in Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="a0215-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="a0215-106">Ciò significa che il codice di errore WSAEINPROGRESS non verrà mai indicato e che le funzioni di Windows Sockets 1,1 seguenti non sono disponibili per le applicazioni Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="a0215-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="a0215-107">WSACancelBlockingCall</span><span class="sxs-lookup"><span data-stu-id="a0215-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="a0215-108">WSAIsBlocking</span><span class="sxs-lookup"><span data-stu-id="a0215-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="a0215-109">WSASetBlockingHook</span><span class="sxs-lookup"><span data-stu-id="a0215-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="a0215-110">WSAUnhookBlockingHook</span><span class="sxs-lookup"><span data-stu-id="a0215-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="a0215-111">I programmi Windows Sockets 1,1 scritti per utilizzare lo pseudo-blocco continueranno a funzionare correttamente perché si collegano a Winsock.dll o Wsock32.dll.</span><span class="sxs-lookup"><span data-stu-id="a0215-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="a0215-112">Entrambe continuano a supportare il set completo di funzioni Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="a0215-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="a0215-113">Per consentire ai programmi di diventare applicazioni Windows Sockets 2, è necessario che si verifichino alcune modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="a0215-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="a0215-114">Nella maggior parte dei casi, l'uso oculato dei thread può essere sostituito per supportare l'elaborazione eseguita con una funzione hook di blocco.</span><span class="sxs-lookup"><span data-stu-id="a0215-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 



