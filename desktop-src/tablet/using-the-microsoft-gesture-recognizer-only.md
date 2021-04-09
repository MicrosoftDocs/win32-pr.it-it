---
description: "È possibile utilizzare un agente di raccolta input penna (InkCollector, InkOverlay o InkPicture) per accedere direttamente al riconoscitore di movimento Microsoft predefinito. Per utilizzare un agente di raccolta input penna per accedere al riconoscimento movimento: impostare la proprietà CollectionMode dell'agente di raccolta input penna su InkAndGesture mode o GestureOnly mode. inkOverlay. CollectionMode = CollectionMode. GestureOnly; Scegliere il movimento che si desidera supportare. inkOverlay. SetGestureStatus (ApplicationGesture. AllGestures, true); implementare un gestore eventi che riceve le notifiche di movimento. Nel gestore eventi è necessario implementare l'azione corrispondente a ogni evento ricevuto. Nota la modalità mista supporta solo movimenti a tratto singolo. La modalità movimento supporta più movimenti Stroke. inkOverlay. Gesture + = new InkCollectorGestureEventHandler ( \\_ gesto InkOverlay); in modalità InkAndGesture ogni singolo tratto viene inviato al riconoscitore di movimento Microsoft. Se viene riconosciuta come un movimento abilitato, viene inviata una notifica degli eventi. Se l'applicazione accetta la notifica degli eventi, il tratto verrà cancellato. Se l'applicazione non accetta la notifica o se il tratto non è riconosciuto come un movimento, il tratto viene archiviato nell'oggetto input penna. In modalità GestureOnly, i tratti sono delimitati da timeout prima e dopo i tratti. I tratti raccolti nel timeout vengono inviati al riconoscimento. Se i tratti sono riconosciuti come un movimento abilitato, viene inviata una notifica degli eventi. L'applicazione può accettare o rifiutare l'evento, effettuando o meno l'azione corrispondente. In modalità solo movimento, i tratti non vengono mai salvati nell'oggetto input penna."
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Uso del riconoscimento di Microsoft gesture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879134"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="bf6d1-113">Uso del riconoscimento di Microsoft gesture</span><span class="sxs-lookup"><span data-stu-id="bf6d1-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="bf6d1-114">È possibile utilizzare un agente di raccolta input penna ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)o [InkPicture](inkpicture-control-reference.md)) per accedere direttamente al riconoscitore di movimento Microsoft predefinito.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="bf6d1-115">Per usare un agente di raccolta input penna per accedere al riconoscimento movimento:</span><span class="sxs-lookup"><span data-stu-id="bf6d1-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="bf6d1-116">Impostare la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) dell'agente di raccolta input penna su modalità **InkAndGesture** o **GestureOnly** .</span><span class="sxs-lookup"><span data-stu-id="bf6d1-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="bf6d1-117">Scegliere il movimento che si desidera supportare.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="bf6d1-118">Implementare un gestore eventi che riceve le notifiche di movimento.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="bf6d1-119">Nel gestore eventi è necessario implementare l'azione corrispondente a ogni evento ricevuto.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="bf6d1-120">La modalità mista supporta solo movimenti a tratto singolo.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="bf6d1-121">La modalità movimento supporta più movimenti Stroke.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="bf6d1-122">In modalità **InkAndGesture** ogni singolo tratto viene inviato al riconoscitore di movimento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="bf6d1-123">Se viene riconosciuta come un movimento abilitato, viene inviata una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="bf6d1-124">Se l'applicazione accetta la notifica degli eventi, il tratto verrà cancellato.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="bf6d1-125">Se l'applicazione non accetta la notifica o se il tratto non è riconosciuto come un movimento, il tratto viene archiviato nell'oggetto [**input penna**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="bf6d1-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="bf6d1-126">In modalità **GestureOnly** , i tratti sono delimitati da timeout prima e dopo i tratti.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="bf6d1-127">I tratti raccolti nel timeout vengono inviati al riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="bf6d1-128">Se i tratti sono riconosciuti come un movimento abilitato, viene inviata una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="bf6d1-129">L'applicazione può accettare o rifiutare l'evento, effettuando o meno l'azione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bf6d1-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="bf6d1-130">In modalità solo movimento, i tratti non vengono mai salvati nell'oggetto [**input penna**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="bf6d1-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf6d1-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf6d1-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bf6d1-132">[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bf6d1-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="bf6d1-133">[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bf6d1-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="bf6d1-134">[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="bf6d1-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
