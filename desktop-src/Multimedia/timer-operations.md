---
title: Operazioni di eventi timer
description: Operazioni di eventi timer
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- timer multimediali, eventi
- timer, eventi
- Funzione timeSetEvent (funzione)
- timeKillEvent (funzione)
- avvio di eventi timer
- eventi timer singolo
- eventi timer periodici
- annullamento degli eventi del timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724799"
---
# <a name="timer-event-operations"></a><span data-ttu-id="293ee-111">Operazioni di eventi timer</span><span class="sxs-lookup"><span data-stu-id="293ee-111">Timer Event Operations</span></span>

<span data-ttu-id="293ee-112">Dopo aver stabilito la risoluzione del timer dell'applicazione, è possibile avviare gli eventi del timer usando la funzione [**funzione timeSetEvent**](/previous-versions//dd757634(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="293ee-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="293ee-113">Questa funzione restituisce un identificatore del timer che può essere utilizzato per arrestare o identificare gli eventi del timer.</span><span class="sxs-lookup"><span data-stu-id="293ee-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="293ee-114">Uno dei parametri della funzione è l'indirizzo di una funzione di callback [**TimeProc**](/previous-versions//dd757631(v=vs.85)) che viene chiamata quando si verifica l'evento del timer.</span><span class="sxs-lookup"><span data-stu-id="293ee-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="293ee-115">Esistono due tipi di eventi del timer: *singolo* e *periodico*.</span><span class="sxs-lookup"><span data-stu-id="293ee-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="293ee-116">Un singolo evento del timer si verifica una sola volta, dopo un numero specificato di millisecondi.</span><span class="sxs-lookup"><span data-stu-id="293ee-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="293ee-117">Un evento timer periodico si verifica ogni volta che trascorre un numero specificato di millisecondi.</span><span class="sxs-lookup"><span data-stu-id="293ee-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="293ee-118">L'intervallo tra gli eventi periodici è denominato *ritardo evento*.</span><span class="sxs-lookup"><span data-stu-id="293ee-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="293ee-119">Gli eventi timer periodici con un ritardo evento di 10 millisecondi o meno utilizzano una parte significativa delle risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="293ee-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="293ee-120">La relazione tra la risoluzione di un evento timer e la lunghezza del ritardo dell'evento è importante negli eventi del timer.</span><span class="sxs-lookup"><span data-stu-id="293ee-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="293ee-121">Se ad esempio si specifica una risoluzione di 5 e un ritardo evento 100, i servizi timer inviano una notifica alla funzione di callback dopo un intervallo compreso tra 95 e 105 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="293ee-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="293ee-122">È possibile annullare un evento del timer attivo in qualsiasi momento tramite la funzione [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="293ee-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="293ee-123">Assicurarsi di annullare tutti i timer in attesa prima di liberare la memoria che contiene la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="293ee-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="293ee-124">Il timer multimediale viene eseguito nel proprio thread.</span><span class="sxs-lookup"><span data-stu-id="293ee-124">The multimedia timer runs in its own thread.</span></span>

 

 

 