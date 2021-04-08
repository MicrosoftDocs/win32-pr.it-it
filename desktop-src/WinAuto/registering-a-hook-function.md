---
title: Registrazione di una funzione hook
description: Le applicazioni client ricevono WinEvents in una funzione di callback WinEventProc. Le azioni eseguite dalla funzione di callback sono definite dall'applicazione, ma la sintassi deve essere quella specificata nel prototipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855778"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="5e4a4-104">Registrazione di una funzione hook</span><span class="sxs-lookup"><span data-stu-id="5e4a4-104">Registering a Hook Function</span></span>

<span data-ttu-id="5e4a4-105">Le applicazioni client ricevono WinEvents in una funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) .</span><span class="sxs-lookup"><span data-stu-id="5e4a4-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="5e4a4-106">Le azioni eseguite dalla funzione di callback sono definite dall'applicazione, ma la sintassi deve essere quella specificata nel prototipo.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="5e4a4-107">Prima di poter ricevere gli eventi, la funzione deve essere registrata chiamando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span><span class="sxs-lookup"><span data-stu-id="5e4a4-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="5e4a4-108">Il client può chiamare **SetWinEventHook** più di una volta per registrare funzioni hook diverse o per impostare eventi aggiuntivi per una funzione hook registrata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="5e4a4-109">Quando si chiama [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , il client specifica quali eventi ricevere e come riceverli.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="5e4a4-110">Il client può scegliere di:</span><span class="sxs-lookup"><span data-stu-id="5e4a4-110">The client can choose to:</span></span>

-   <span data-ttu-id="5e4a4-111">Ricevere tutti gli eventi o un set di eventi specifico.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="5e4a4-112">Ricevere eventi da tutti i thread o da un thread specifico.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="5e4a4-113">Ricevere eventi da tutti i processi o da un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="5e4a4-114">Gestione degli eventi in corso o out-of-process.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="5e4a4-115">Quando viene generato un evento che corrisponde ai criteri specificati, il sistema chiama la funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) del client (o "procedura hook").</span><span class="sxs-lookup"><span data-stu-id="5e4a4-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="5e4a4-116">I parametri ricevuti dalla funzione hook indicano al client la finestra, l'oggetto e il possibile elemento figlio che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="5e4a4-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="5e4a4-117">Un client usa questi parametri in una chiamata di recupero di oggetti, ad esempio [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="5e4a4-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




