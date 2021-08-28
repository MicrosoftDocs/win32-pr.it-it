---
description: L'oggetto RealTimeStylus non raccoglie intrinsecamente l'input penna. Per usare RealTimeStylus per raccogliere input penna, creare un plug-in dell'agente di raccolta input penna.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64966e2d088e9145fa4a0c0b29a7f7cc787b8435a3e4a609e75eae27b4e25524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967210"
---
# <a name="ink-collection-plug-ins"></a>Ink-Collection plug-in

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) non raccoglie intrinsecamente l'input penna. Per usare **RealTimeStylus per** raccogliere input penna, creare un plug-in dell'agente di raccolta input penna.

Di seguito è riportato uno scenario minimo per l'uso [**dell'oggetto RealTimeStylus**](realtimestylus-class.md) in un modulo che raccoglie input penna.

1.  Creare un modulo che implementa [**l'interfaccia IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
2.  Creare un [**oggetto RealTimeStylus**](realtimestylus-class.md) e collegarlo a un controllo nel form.
3.  Impostare l'interesse per le notifiche StylusDown, Packets e StylusUp nella proprietà [Data Interest del](/previous-versions/ms574886(v=vs.100)) modulo.
4.  Nei metodi [**StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del form aggiungere codice per gestire le notifiche relative a stilo verso il basso, pacchetti e stilo verso l'alto inviate dall'oggetto [**RealTimeStylus del**](realtimestylus-class.md) form. Questo codice deve archiviare i dati della penna e creare e archiviare i tratti.

Per un esempio di un'applicazione di questo tipo, vedere [l'esempio di raccolta di input penna RealTimeStylus.](realtimestylus-ink-collection-sample.md)

> [!Note]  
> Quando si [verifica un evento DisplaySettingsChanged,](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) chiama il metodo [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) dei tratti raccolti in un gestore eventi DisplaySettingsChanged per ricalcolare le proprietà [Width](/previous-versions/ms582112(v=vs.100)) [e Height.](/previous-versions/ms582106(v=vs.100)) Ciò è necessario per fare in modo che i punti per pollice (dpi) possibili modifiche che derivano dall'evento DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Raccolta input penna e riconoscitori

Né l'analisi dell'input penna né il riconoscimento della grafia sono una [**funzione dell'oggetto RealTimeStylus.**](realtimestylus-class.md) Poiché il plug-in dell'agente di raccolta input penna raccoglie input penna o quando si vuole riconoscere l'input penna, è possibile copiare l'input penna in un oggetto [RecognizerContext](/previous-versions/ms552546(v=vs.100)) [o Divider.](/previous-versions/ms583616(v=vs.100)) Per altre informazioni sul riconoscimento e l'analisi dell'input penna, vedere [About Handwriting Recognition (Informazioni sul riconoscimento](about-handwriting-recognition.md) della [grafia) o The Divider Object (Oggetto divider).](the-divider-object.md)

## <a name="static-rendering"></a>Rendering statico

Per eseguire il rendering dell'input penna durante la raccolta, collegare un [oggetto DynamicRenderer](/previous-versions/ms575176(v=vs.100)) [**all'oggetto RealTimeStylus.**](realtimestylus-class.md) Per eseguire il rendering dell'input penna dopo che è stato raccolto, usa un [oggetto Renderer](/previous-versions/ms552630(v=vs.100)) per disegnare i tratti nell'oggetto [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) appropriato. Per altre informazioni sull'oggetto DynamicRenderer, vedere [Dynamic-Renderer Plug-ins](dynamic-renderer-plug-ins.md). Per un esempio di rendering statico e dinamico, vedere [RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md).

 

 
