---
description: In questo argomento vengono illustrati i timer. Un timer è una routine interna che misura ripetutamente un intervallo specificato, in millisecondi.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318354"
---
# <a name="timers"></a><span data-ttu-id="d2349-104">Timer</span><span class="sxs-lookup"><span data-stu-id="d2349-104">Timers</span></span>

<span data-ttu-id="d2349-105">Un timer è una routine interna che misura ripetutamente un intervallo specificato, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="d2349-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="d2349-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d2349-106">In This Section</span></span>



| <span data-ttu-id="d2349-107">Nome</span><span class="sxs-lookup"><span data-stu-id="d2349-107">Name</span></span>                                   | <span data-ttu-id="d2349-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2349-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2349-109">Informazioni sui timer</span><span class="sxs-lookup"><span data-stu-id="d2349-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="d2349-110">Viene descritto come creare, identificare, impostare ed eliminare i timer.</span><span class="sxs-lookup"><span data-stu-id="d2349-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="d2349-111">Utilizzo di timer</span><span class="sxs-lookup"><span data-stu-id="d2349-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="d2349-112">Viene illustrato come creare ed eliminare i timer e come utilizzare un timer per intercettare l'input del mouse a intervalli specificati.</span><span class="sxs-lookup"><span data-stu-id="d2349-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="d2349-113">Riferimento timer</span><span class="sxs-lookup"><span data-stu-id="d2349-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="d2349-114">Contiene il riferimento all'API.</span><span class="sxs-lookup"><span data-stu-id="d2349-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="d2349-115">Funzioni timer</span><span class="sxs-lookup"><span data-stu-id="d2349-115">Timer Functions</span></span>



| <span data-ttu-id="d2349-116">Nome</span><span class="sxs-lookup"><span data-stu-id="d2349-116">Name</span></span>                           | <span data-ttu-id="d2349-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2349-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2349-118">**KillTimer**</span><span class="sxs-lookup"><span data-stu-id="d2349-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="d2349-119">Elimina il timer specificato.</span><span class="sxs-lookup"><span data-stu-id="d2349-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="d2349-120">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="d2349-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="d2349-121">Crea un timer con il valore di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="d2349-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="d2349-122">*TimerProc*</span><span class="sxs-lookup"><span data-stu-id="d2349-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="d2349-123">Funzione di callback definita dall'applicazione che elabora i messaggi del [**\_ timer WM**](wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="d2349-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="d2349-124">Il tipo **TIMERPROC** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="d2349-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="d2349-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2349-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="d2349-126">Notifiche timer</span><span class="sxs-lookup"><span data-stu-id="d2349-126">Timer Notifications</span></span>



| <span data-ttu-id="d2349-127">Nome</span><span class="sxs-lookup"><span data-stu-id="d2349-127">Name</span></span>                          | <span data-ttu-id="d2349-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2349-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2349-129">**\_timer WM**</span><span class="sxs-lookup"><span data-stu-id="d2349-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="d2349-130">Inserito nella coda di messaggi del thread di installazione quando scade un timer.</span><span class="sxs-lookup"><span data-stu-id="d2349-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="d2349-131">Il messaggio viene inserito dalla funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="d2349-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
