---
description: L'oggetto RealTimeStylus non raccoglie intrinsecamente input penna. Per usare RealTimeStylus per raccogliere input penna, creare un plug-in dell'agente di raccolta input penna.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Plug-in Ink-Collection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878742"
---
# <a name="ink-collection-plug-ins"></a>Plug-in Ink-Collection

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) non raccoglie intrinsecamente input penna. Per usare **RealTimeStylus** per raccogliere input penna, creare un plug-in dell'agente di raccolta input penna.

Di seguito è riportato uno scenario minimo per l'utilizzo dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) in un modulo che raccoglie l'input penna.

1.  Creare un form che implementi l'interfaccia [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Creare un oggetto [**RealTimeStylus**](realtimestylus-class.md) e collegarlo a un controllo nel form.
3.  Impostare interesse per le notifiche StylusDown, pacchetti e StylusUp nella proprietà [DataInterest](/previous-versions/ms574886(v=vs.100)) del modulo.
4.  Nei metodi [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del modulo, aggiungere il codice per gestire lo stilo, i pacchetti e le notifiche dello stilo, che vengono inviati dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) del modulo. Questo codice deve archiviare i dati della penna e creare e archiviare i tratti.

Per un esempio di tale applicazione, vedere l'esempio [RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md) .

> [!Note]  
> Quando si verifica un evento [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) , chiamare il metodo [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) dei tratti raccolti in un gestore eventi DisplaySettingsChanged per ricalcolare le proprietà [Width](/previous-versions/ms582112(v=vs.100)) e [Height](/previous-versions/ms582106(v=vs.100)) . Questa operazione è necessaria per tenere conto di possibili modifiche di punti per pollice (dpi) derivanti dall'evento DisplaySettingsChanged.

 

## <a name="ink-collection-and-recognizers"></a>Raccolta e riconoscitori di input penna

Né l'analisi dell'input penna né il riconoscimento della grafia sono una funzione dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) . Quando il plug-in dell'agente di raccolta input penna raccoglie input penna o si desidera riconoscere l'input penna, è possibile copiare l'input penna in un oggetto [RecognizerContext](/previous-versions/ms552546(v=vs.100)) o [Divider](/previous-versions/ms583616(v=vs.100)) . Per ulteriori informazioni sull'analisi dei riconoscimenti e dell'input penna, vedere [informazioni sul riconoscimento della grafia](about-handwriting-recognition.md) o [sull'oggetto divisore](the-divider-object.md).

## <a name="static-rendering"></a>Rendering statico

Per eseguire il rendering dell'input penna mentre viene raccolto, alleghi un oggetto [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) all'oggetto [**RealTimeStylus**](realtimestylus-class.md) . Per eseguire il rendering dell'input penna dopo che è stato raccolto, utilizzare un oggetto [renderer](/previous-versions/ms552630(v=vs.100)) per tracciare i tratti nell'oggetto [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) appropriato. Per ulteriori informazioni sull'oggetto DynamicRenderer, vedere [plug-in Dynamic-renderer](dynamic-renderer-plug-ins.md). Per un esempio di rendering statico e dinamico, vedere [esempio di raccolta input penna di RealTimeStylus](realtimestylus-ink-collection-sample.md).

 

 
