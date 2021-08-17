---
description: Panoramica delle considerazioni generali sul threading.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Considerazioni generali sul threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092575"
---
# <a name="general-threading-considerations"></a>Considerazioni generali sul threading

Di seguito sono riportate considerazioni generali sul threading durante lo sviluppo per Tablet PC.

-   [Thread dell'applicazione e non dell'applicazione](#application-and-non-application-threads)
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

## <a name="application-and-non-application-threads"></a>Thread dell'applicazione e non dell'applicazione

Tutti gli eventi di input penna vengono generati in un thread di input penna separato con priorità alta. In questo modo l'input penna può fluire senza problemi anche quando un'applicazione viene eseguita lentamente. Tuttavia, i gestori eventi possono rallentare o bloccare il rendering dell'input penna.

Tutti gli eventi di riconoscimento generati dalle chiamate al metodo di riconoscimento in background vengono gestiti in un thread separato di riconoscimento in background con priorità normale.

Tutti gli eventi del mouse vengono generati nel thread principale dell'interfaccia utente dell'applicazione.

## <a name="performance-considerations"></a>Considerazioni sulle prestazioni

### <a name="event-handlers"></a>Gestori di eventi

L'API (Application Programming Interface) della piattaforma Tablet PC include un modello interattivo per gli eventi anziché un modello di notifica. Mantenere il codice nei gestori eventi breve per ridurre il tempo di blocco del rendering dell'input penna. La raccolta di input penna dal Tablet PC non è bloccata, ma l'applicazione non riceve l'input penna mentre l'applicazione è bloccata.

### <a name="autoredraw-property"></a>Proprietà AutoRedraw

Quando l'applicazione esegue il rendering personalizzato o quando l'applicazione è sensibile ai problemi di disegno, è possibile gestire il ridisegno e impostare la proprietà [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) su **false** per l'oggetto [**InkCollector,**](inkcollector-class.md) [**l'oggetto InkOverlay**](inkoverlay-class.md) o il [controllo InkPicture.](inkpicture-control.md) Usare gli eventi nella tabella seguente per gestire il ridisegno.



| Oggetto o controllo                                            | Evento                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Oggetto<br/> | Gli eventi [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control.Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del controllo sottostante.<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Oggetto<br/>     | Gli eventi [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control.Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del controllo sottostante.<br/>                                 |
| [InkPicture](inkpicture-control.md) Controllo<br/>      | Eventi [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) e [Control.Paint ereditati del controllo](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) [InkPicture.](inkpicture-control.md)<br/> |



 

### <a name="dynamicrendering-property"></a>Proprietà DynamicRendering

Quando l'applicazione esegue il rendering personalizzato o quando si vogliono le informazioni, ma non l'input penna, è possibile gestire manualmente la disposizione dell'input penna e disattivare il rendering in tempo reale dell'input penna impostando la proprietà [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) su **false** per l'oggetto [**InkCollector,**](inkcollector-class.md) [**l'oggetto InkOverlay**](inkoverlay-class.md) o il [controllo InkPicture.](inkpicture-control.md)

## <a name="event-threading-considerations"></a>Considerazioni sul threading degli eventi

Gli eventi API della piattaforma Tablet PC vengono generati in vari thread.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>Eventi degli oggetti InkCollector e InkOverlay

La maggior parte degli eventi dell'oggetto [**InkCollector**](inkcollector-class.md) e [**InkOverlay**](inkoverlay-class.md) viene generata sul thread di input penna. Solo gli eventi del mouse per questi oggetti vengono generati nel thread dell'interfaccia utente. Ad esempio, per **l'oggetto InkCollector,** l'evento [**MouseDown**](inkcollector-mousedown.md) viene generato nel thread dell'interfaccia utente e l'evento [**CursorDown**](inkcollector-cursordown.md) viene generato sul thread di input penna.

### <a name="ink-object-and-strokes-collection-events"></a>Eventi dell'oggetto Ink e della raccolta Strokes

Gli [**eventi dell'oggetto**](inkdisp-class.md) Ink e della raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) possono derivare dal thread di input penna o dal thread dell'interfaccia utente. Quando l'applicazione modifica **l'oggetto Ink** o **la raccolta Strokes,** l'evento viene generato nel thread dell'interfaccia utente. Quando [**l'oggetto InkCollector**](inkcollector-class.md) o [**l'oggetto InkOverlay**](inkoverlay-class.md) aggiorna l'oggetto **Ink** o la raccolta **Strokes,** l'evento viene generato nel thread di input penna.

I [controlli InkPicture](inkpicture-control-reference.md) [e InkEdit](inkedit-control-reference.md) operano in un apartment a thread singolo (STA). Quando il controllo InkPicture o InkEdit aggiorna [**l'oggetto Ink**](inkdisp-class.md) o la raccolta [**Strokes,**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) l'evento viene generato nel thread dell'interfaccia utente.

### <a name="recognition-events"></a>Eventi di riconoscimento

Gli eventi di riconoscimento vengono generati nel thread dell'interfaccia utente o nel thread di riconoscimento in background.

-   Il metodo Recognize [](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) del controllo [InkEdit](inkedit-control-reference.md) genera l'evento [Recognition](/previous-versions/ms836436(v=msdn.10)) (solo Libreria gestita) o [**RecognitionResult**](inkedit-recognitionresult.md) (solo Automazione) nel thread dell'interfaccia utente.
-   I metodi [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) e [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) generano gli eventi [**Recognition**](inkrecognizercontext-recognition.md) e [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) nel thread di riconoscimento in background.

### <a name="pen-input-panel-events"></a>Eventi del pannello input penna

[**Gli eventi PenInputPanel**](peninputpanel-class.md) vengono generati nel thread in cui viene creato l'oggetto **PenInputPanel.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft.Ink.InkCollector.DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft.Ink.InkCollector.AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

