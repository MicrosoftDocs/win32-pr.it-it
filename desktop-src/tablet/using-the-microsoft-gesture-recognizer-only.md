---
description: "È possibile usare un agente di raccolta input penna (InkCollector, InkOverlay o InkPicture) per accedere direttamente al riconoscimento dei movimenti Microsoft predefinito. Per usare un agente di raccolta input penna per accedere al riconoscimento dei movimenti: impostare la proprietà CollectionMode dell'agente di raccolta input penna sulla modalità InkAndGesture o GestureOnly.inkOverlay.CollectionMode = CollectionMode.GestureOnly; Scegliere il movimento che si vuole supportare.inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);Implementare un gestore eventi che riceve le notifiche dei movimenti. Nel gestore eventi è necessario implementare l'azione corrispondente a ogni evento ricevuto. Nota La modalità mista supporta solo i movimenti a tratto singolo. La modalità movimento supporta più movimenti del tratto. inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay Gesture);In modalità InkAndGesture ogni singolo tratto viene inviato al riconoscitore \\_ movimenti Microsoft. Se viene riconosciuto come movimento abilitato, viene inviata una notifica di evento. Se l'applicazione accetta la notifica dell'evento, il tratto viene cancellato. Se l'applicazione non accetta la notifica o se il tratto non è riconosciuto come movimento, il tratto viene archiviato nell'oggetto Ink. In modalità GestureOnly i tratti sono delimitati da timeout prima e dopo i tratti. I tratti raccolti entro il timeout vengono inviati al riconoscitore. Se i tratti vengono riconosciuti come movimenti abilitati, viene inviata una notifica dell'evento. L'applicazione può accettare o rifiutare l'evento, in base all'azione corrispondente. In modalità solo movimento, i tratti non vengono mai salvati nell'oggetto Ink."
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Uso solo di Riconoscimento movimenti Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d7b27ae30e0bba98ee2c9db57cc0da2d6491932d0137cc5cd4d2b6f86420ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715178"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Uso solo di Riconoscimento movimenti Microsoft

È possibile usare un agente di raccolta input penna ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)o [InkPicture](inkpicture-control-reference.md)) per accedere direttamente al riconoscimento dei movimenti Microsoft predefinito.

Per usare un agente di raccolta input penna per accedere al riconoscimento movimenti:

-   Impostare la [**proprietà CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) dell'agente di raccolta input penna **sulla modalità InkAndGesture** o **GestureOnly.**

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Scegliere il movimento che si vuole supportare.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implementare un gestore eventi che riceve le notifiche dei movimenti. Nel gestore eventi è necessario implementare l'azione corrispondente a ogni evento ricevuto.
    > [!Note]  
    > La modalità mista supporta solo movimenti a tratto singolo. La modalità movimento supporta più movimenti del tratto.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

In **modalità InkAndGesture** ogni singolo tratto viene inviato al riconoscitore movimenti Microsoft. Se viene riconosciuto come movimento abilitato, viene inviata una notifica di evento. Se l'applicazione accetta la notifica dell'evento, il tratto viene cancellato. Se l'applicazione non accetta la notifica o se il tratto non è riconosciuto come movimento, il tratto viene archiviato [**nell'oggetto Ink.**](inkdisp-class.md)

In **modalità GestureOnly** i tratti sono delimitati da timeout prima e dopo i tratti. I tratti raccolti entro il timeout vengono inviati al riconoscitore. Se i tratti vengono riconosciuti come movimenti abilitati, viene inviata una notifica dell'evento. L'applicazione può accettare o rifiutare l'evento, in base all'azione corrispondente. In modalità solo movimento, i tratti non vengono mai salvati [**nell'oggetto Ink.**](inkdisp-class.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
