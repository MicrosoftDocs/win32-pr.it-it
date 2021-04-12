---
description: Panoramica delle considerazioni generali relative al threading.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Considerazioni generali sul threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f825ec7a1397dae7d60aa14b31603ee76a2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526586"
---
# <a name="general-threading-considerations"></a>Considerazioni generali sul threading

Di seguito sono riportate considerazioni generali relative al threading quando si sviluppa per Tablet PC.

-   [Thread applicazione e non applicazione](#application-and-non-application-threads)
-   [Considerazioni sulle prestazioni](#performance-considerations)
    -   [Gestori eventi](#event-handlers)
    -   [Proprietà AutoRedraw](#autoredraw-property)
    -   [Proprietà DynamicRendering](#dynamicrendering-property)
-   [Considerazioni sul threading degli eventi](#event-threading-considerations)
    -   [Eventi degli oggetti InkCollector e InkOverlay](#inkcollector-and-inkoverlay-objects-events)
    -   [Eventi dell'oggetto Ink e della raccolta Strokes](#ink-object-and-strokes-collection-events)
    -   [Eventi di riconoscimento](#recognition-events)
    -   [Eventi del pannello input penna](#pen-input-panel-events)
-   [Argomenti correlati](#related-topics)

## <a name="application-and-non-application-threads"></a>Thread applicazione e non applicazione

Tutti gli eventi Ink vengono generati in un thread di input penna separato a priorità alta. In questo modo, l'input penna potrebbe propagarsi senza problemi anche quando un'applicazione viene eseguita lentamente. Tuttavia, i gestori eventi possono rallentare o bloccare il rendering dell'input penna.

Tutti gli eventi di riconoscimento generati dalle chiamate al metodo di riconoscimento in background vengono gestiti in un thread di riconoscimento in background separato con priorità normale.

Tutti gli eventi del mouse vengono generati sul thread dell'interfaccia utente principale dell'applicazione.

## <a name="performance-considerations"></a>Considerazioni sulle prestazioni

### <a name="event-handlers"></a>Gestori di eventi

La piattaforma Tablet PC Application Programming Interface (API) dispone di un modello interattivo per gli eventi anziché un modello di notifica. Per ridurre il tempo di blocco del rendering dell'input penna, è possibile lasciare il codice nei gestori eventi Short. La raccolta di input penna da parte del Tablet PC non è bloccata, ma l'applicazione non riceve l'input penna mentre l'applicazione è bloccata.

### <a name="autoredraw-property"></a>Proprietà AutoRedraw

Quando l'applicazione esegue il rendering personalizzato o quando l'applicazione è sensibile ai problemi di disegno, è possibile gestire il disegno e impostare la proprietà [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) su **false** per l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control.md) . Utilizzare gli eventi nella tabella seguente per gestire la ridisegno.



| Oggetto o controllo                                            | Evento                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Oggetto [**InkCollector**](inkcollector-class.md) Oggetto<br/> | Il controllo del controllo sottostante. gli eventi [invalidati](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Oggetto<br/>     | Il controllo del controllo sottostante. gli eventi [invalidati](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/>                                 |
| [InkPicture](inkpicture-control.md) Controllo<br/>      | Il controllo ereditato del controllo [InkPicture](inkpicture-control.md) . gli eventi [invalidati](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) .<br/> |



 

### <a name="dynamicrendering-property"></a>Proprietà DynamicRendering

Quando l'applicazione esegue il rendering personalizzato o quando si desiderano le informazioni, ma non l'input penna, è possibile gestire il layout dell'input penna e disattivare il rendering in tempo reale dell'input penna impostando la proprietà [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) su **false** per l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control.md) .

## <a name="event-threading-considerations"></a>Considerazioni sul threading degli eventi

Gli eventi API della piattaforma Tablet PC vengono generati in diversi thread.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Eventi degli oggetti InkCollector e InkOverlay

La maggior parte degli eventi degli oggetti [**InkCollector**](inkcollector-class.md) e [**InkOverlay**](inkoverlay-class.md) viene generata nel thread di input penna. Solo gli eventi del mouse per questi oggetti vengono generati sul thread dell'interfaccia utente. Per l'oggetto **InkCollector** , ad esempio, viene generato l'evento [**MouseDown**](inkcollector-mousedown.md) sul thread dell'interfaccia utente e viene generato l'evento [**CursorDown**](inkcollector-cursordown.md) sul thread Ink.

### <a name="ink-object-and-strokes-collection-events"></a>Eventi dell'oggetto Ink e della raccolta Strokes

Gli eventi dell'oggetto [**Ink**](inkdisp-class.md) e della raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) possono provenire dal thread dell'input penna o dal thread dell'interfaccia utente. Quando l'applicazione modifica l'oggetto **Ink** o la raccolta **Strokes** , l'evento viene generato nel thread UI. Quando l'oggetto [**InkCollector**](inkcollector-class.md) o l'oggetto [**InkOverlay**](inkoverlay-class.md) aggiorna l'oggetto **Ink** o la raccolta **Strokes** , l'evento viene generato nel thread di input penna.

I controlli [InkPicture](inkpicture-control-reference.md) e [InkEdit](inkedit-control-reference.md) operano in un Apartment a thread singolo (sta). Quando il controllo InkPicture o InkEdit aggiorna l'oggetto [**Ink**](inkdisp-class.md) o la raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , l'evento viene generato sul thread dell'interfaccia utente.

### <a name="recognition-events"></a>Eventi di riconoscimento

Gli eventi di riconoscimento vengono generati nel thread UI o nel thread di riconoscimento in background.

-   Il metodo [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) del controllo [InkEdit](inkedit-control-reference.md) genera l'evento di [riconoscimento](/previous-versions/ms836436(v=msdn.10)) (solo libreria gestita) o [**RECOGNITIONRESULT**](inkedit-recognitionresult.md) (solo automazione) nel thread UI.
-   I metodi [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) e [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) generano gli eventi di [**riconoscimento**](inkrecognizercontext-recognition.md) e di [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) nel thread di riconoscimento in background.

### <a name="pen-input-panel-events"></a>Eventi del pannello input penna

Gli eventi [**PenInputPanel**](peninputpanel-class.md) vengono generati sul thread in cui viene creato l'oggetto **PenInputPanel** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink. InkCollector. DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft. Ink. InkCollector. AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

