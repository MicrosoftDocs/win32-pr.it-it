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
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Uso del riconoscimento di Microsoft gesture

È possibile utilizzare un agente di raccolta input penna ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)o [InkPicture](inkpicture-control-reference.md)) per accedere direttamente al riconoscitore di movimento Microsoft predefinito.

Per usare un agente di raccolta input penna per accedere al riconoscimento movimento:

-   Impostare la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) dell'agente di raccolta input penna su modalità **InkAndGesture** o **GestureOnly** .

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Scegliere il movimento che si desidera supportare.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implementare un gestore eventi che riceve le notifiche di movimento. Nel gestore eventi è necessario implementare l'azione corrispondente a ogni evento ricevuto.
    > [!Note]  
    > La modalità mista supporta solo movimenti a tratto singolo. La modalità movimento supporta più movimenti Stroke.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

In modalità **InkAndGesture** ogni singolo tratto viene inviato al riconoscitore di movimento Microsoft. Se viene riconosciuta come un movimento abilitato, viene inviata una notifica degli eventi. Se l'applicazione accetta la notifica degli eventi, il tratto verrà cancellato. Se l'applicazione non accetta la notifica o se il tratto non è riconosciuto come un movimento, il tratto viene archiviato nell'oggetto [**input penna**](inkdisp-class.md) .

In modalità **GestureOnly** , i tratti sono delimitati da timeout prima e dopo i tratti. I tratti raccolti nel timeout vengono inviati al riconoscimento. Se i tratti sono riconosciuti come un movimento abilitato, viene inviata una notifica degli eventi. L'applicazione può accettare o rifiutare l'evento, effettuando o meno l'azione corrispondente. In modalità solo movimento, i tratti non vengono mai salvati nell'oggetto [**input penna**](inkdisp-class.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
