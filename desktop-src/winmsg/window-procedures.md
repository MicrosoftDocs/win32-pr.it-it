---
description: In questa sezione vengono descritte le procedure di finestra. A ogni finestra è associata una routine di finestra che elabora tutti i messaggi inviati o inviati a tutte le finestre della classe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Routine della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317861"
---
# <a name="window-procedures"></a><span data-ttu-id="546bb-104">Routine della finestra</span><span class="sxs-lookup"><span data-stu-id="546bb-104">Window Procedures</span></span>

<span data-ttu-id="546bb-105">A ogni finestra è associata una routine della finestra, una funzione che elabora tutti i messaggi inviati o inviati a tutte le finestre della classe.</span><span class="sxs-lookup"><span data-stu-id="546bb-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="546bb-106">Tutti gli aspetti dell'aspetto e del comportamento di una finestra dipendono dalla risposta della routine della finestra a questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="546bb-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="546bb-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="546bb-107">In This Section</span></span>



| <span data-ttu-id="546bb-108">Nome</span><span class="sxs-lookup"><span data-stu-id="546bb-108">Name</span></span>                                                         | <span data-ttu-id="546bb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="546bb-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="546bb-110">Informazioni sulle routine della finestra</span><span class="sxs-lookup"><span data-stu-id="546bb-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="546bb-111">Descrive le routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="546bb-111">Discusses window procedures.</span></span> <span data-ttu-id="546bb-112">Ogni finestra è un membro di una particolare classe di finestra.</span><span class="sxs-lookup"><span data-stu-id="546bb-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="546bb-113">La classe Window determina la routine della finestra predefinita utilizzata da una singola finestra per elaborare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="546bb-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="546bb-114">Utilizzo delle routine della finestra</span><span class="sxs-lookup"><span data-stu-id="546bb-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="546bb-115">Viene illustrato come eseguire le attività seguenti associate alle routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="546bb-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="546bb-116">Guida di riferimento alle procedure della finestra</span><span class="sxs-lookup"><span data-stu-id="546bb-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="546bb-117">Contiene il riferimento all'API.</span><span class="sxs-lookup"><span data-stu-id="546bb-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="546bb-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="546bb-118">Functions</span></span>



| <span data-ttu-id="546bb-119">Nome</span><span class="sxs-lookup"><span data-stu-id="546bb-119">Name</span></span>                                     | <span data-ttu-id="546bb-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="546bb-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="546bb-121">**CallWindowProc**</span><span class="sxs-lookup"><span data-stu-id="546bb-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="546bb-122">Passa informazioni sul messaggio alla routine della finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="546bb-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="546bb-123">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="546bb-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="546bb-124">Chiama la routine della finestra predefinita per fornire l'elaborazione predefinita per tutti i messaggi della finestra che un'applicazione non elabora.</span><span class="sxs-lookup"><span data-stu-id="546bb-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="546bb-125">Questa funzione garantisce che ogni messaggio venga elaborato.</span><span class="sxs-lookup"><span data-stu-id="546bb-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="546bb-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) viene chiamato con gli stessi parametri ricevuti dalla routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="546bb-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="546bb-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="546bb-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="546bb-128">Funzione definita dall'applicazione che elabora i messaggi inviati a una finestra.</span><span class="sxs-lookup"><span data-stu-id="546bb-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="546bb-129">Il tipo **WndProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="546bb-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="546bb-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="546bb-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
