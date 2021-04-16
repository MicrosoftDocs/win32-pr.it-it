---
description: Un plug-in di renderer dinamico è un oggetto che Visualizza i dati della penna del tablet in tempo reale poiché è gestito dall'oggetto RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Plug-in Dynamic-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c3f1a33c3cd7faef2e899bcb198ea64aa5bd76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556977"
---
# <a name="dynamic-renderer-plug-ins"></a>Plug-in Dynamic-Renderer

Un plug-in di renderer dinamico è un oggetto che Visualizza i dati della penna del tablet in tempo reale poiché è gestito dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) . In seguito, per gli eventi come un aggiornamento del form, il plug-in di renderer dinamico o un plug-in di agente di raccolta input penna può ricreare l'input penna.

## <a name="the-dynamicrenderer-object"></a>Oggetto DynamicRenderer

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) implementa l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . L'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) esegue il rendering dell'input penna in tempo reale mentre viene disegnato. Quando viene chiamato il metodo [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) mentre l'oggetto **DynamicRenderer** è abilitato, l'oggetto **DynamicRenderer** ritraccia il tratto attualmente raccolto. Inizialmente la proprietà [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) dell'oggetto **DynamicRenderer** è impostata su **false**.

> [!Note]  
> Quando si chiama il metodo [**Refresh**](/previous-versions/ms826370(v=msdn.10)) dell'oggetto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) dall'interno di un gestore eventi [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) nel codice gestito, impostare la proprietà [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10)) dell'oggetto **DynamicRenderer** sulla proprietà [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) dell'oggetto [PaintEventArgs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) .

 

L'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) può memorizzare temporaneamente nella cache i dati dell'input penna. Per usare questa funzionalità nel codice gestito, impostare la proprietà [EnableDataCache](/previous-versions/ms826349(v=msdn.10)) su **true**. Quando l'oggetto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) riceve una chiamata al metodo [**IStylusSyncPlugin. StylusUp**](/previous-versions/ms826366(v=msdn.10)) , memorizza nella cache i dati del tratto e aggiunge dati dello stilo personalizzati alla coda di input in risposta all'oggetto [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) per il tratto. La proprietà [CustomDataId](/previous-versions/ms824749(v=msdn.10)) dell'oggetto [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) è impostata sul valore [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) e la proprietà dati dell'oggetto **CustomStylusData** contiene un oggetto DynamicRendererCachedData. Chiamare il metodo [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) dell'oggetto **DynamicRenderer** dopo che il tratto è stato raccolto e che è possibile eseguirne il rendering in modo statico. Quando viene chiamato il metodo [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) mentre l'oggetto **DynamicRenderer** è abilitato, l'oggetto **DynamicRenderer** ridisegna tutti i tratti memorizzati nella cache. Quando la proprietà [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) è impostata su **false**, i dati del tratto memorizzati nella cache vengono eliminati.

Il diagramma seguente illustra il modo in cui l'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) aggiunge dati ai dati della penna del tablet quando viene impostata la proprietà [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) dell'oggetto **DynamicRenderer** .

![illustrazione che mostra il flusso di dati DynamicRenderer](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

In questo diagramma il cerchio con lettera "SD" rappresenta un oggetto [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) e i cerchi con lettera "P" rappresentano gli oggetti [**pacchetti**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. Il cerchio con lettera "SU" rappresenta un oggetto [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) che l'oggetto **RealTimeStylus** sta attualmente elaborando. Viene inviato alla raccolta di plug-in sincrono e quindi inserito nella coda di output. I cerchi con la lettera "ripristino di emergenza" rappresentano i dati dello stilo personalizzati aggiunti alla coda di input dal plug-in [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) in risposta alla notifica dello stilo in alto associata a "su". I dati di stilo personalizzati con lettera "DR" vengono quindi passati ai plug-in sincroni e quindi alla coda di output prima dell'elaborazione dei successivi dati della penna del tablet. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet. Rappresentata anche nel diagramma è il plug-in dell'agente di raccolta input penna che chiama il metodo [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) dell'oggetto **DynamicRenderer** per rilasciare i dati del tratto memorizzati nella cache dopo l'elaborazione del tratto da parte del plug-in della raccolta di input penna.

### <a name="special-considerations"></a>Considerazioni speciali

Nell'elenco seguente vengono descritti altri punti da considerare quando si usa l'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) .

-   Non è consigliabile alleghi un oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a più di un oggetto [**RealTimeStylus**](realtimestylus-class.md) . Quando due oggetti **RealTimeStylus** a cui è associato l'oggetto **DynamicRenderer** sono abilitati, si verifica quanto segue.

    -   L'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) genera un'eccezione in risposta alla seconda chiamata al metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) .
    -   Il secondo oggetto [**RealTimeStylus**](realtimestylus-class.md) abilitato genera un oggetto [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) e notifica ai rimanenti plug-in le raccolte di plug-in dell'errore.
    -   L'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) interrompe il rendering dei dati della penna del tablet.

-   L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione quando viene chiamato il metodo [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) con il parametro *GUID* impostato sull'identificatore univoco globale (Guid) di DynamicRendererCachedDataGuid.
-   L'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) viene implementato come wrapper Component Object Model (com) e non è possibile chiamare direttamente i metodi dell'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Per ulteriori informazioni sull'operazione COM e sull'oggetto [**RealTimeStylus**](realtimestylus-class.md) , vedere [Note sull'implementazione per le API StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Rendering personalizzato

È possibile creare un plug-in di renderer dinamico personalizzato creando un plug-in sincrono che sottoscrive le notifiche [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) . Il plug-in può quindi eseguire il rendering del tratto mentre viene disegnato. Questo può essere un modo per implementare uno strumento di selezione che usa una selezione in formato libero o una casella di selezione, ad esempio.

 

 
