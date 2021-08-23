---
description: Un plug-in renderer dinamico è un oggetto che visualizza i dati della penna del tablet in tempo reale mentre vengono gestiti dall'oggetto RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Dynamic-Renderer plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6426dfc9f1dae8561802d2cf6c5613fb786600504cc8600046c4df781239abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092683"
---
# <a name="dynamic-renderer-plug-ins"></a>Dynamic-Renderer plug-in

Un plug-in renderer dinamico è un oggetto che visualizza i dati della penna del tablet in tempo reale mentre vengono gestiti [**dall'oggetto RealTimeStylus.**](realtimestylus-class.md) In un secondo momento, per eventi come un aggiornamento del form, il plug-in dynamic-renderer o un plug-in dell'agente di raccolta input penna può ridisegnare l'input penna.

## <a name="the-dynamicrenderer-object"></a>Oggetto DynamicRenderer

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) implementa [**l'interfaccia IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) [**L'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) esegue il rendering dell'input penna in tempo reale, mentre viene disegnato. Quando il [**metodo Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) viene chiamato mentre **l'oggetto DynamicRenderer** è abilitato, l'oggetto **DynamicRenderer** ridisegna il tratto attualmente raccolto. La **proprietà Enabled dell'oggetto DynamicRenderer** è inizialmente impostata su **FALSE.** [](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled)

> [!Note]  
> Quando si chiama il metodo [**Refresh**](/previous-versions/ms826370(v=msdn.10)) dell'oggetto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) dall'interno di un gestore eventi [Paint nel](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) codice gestito, impostare la proprietà [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10)) dell'oggetto **DynamicRenderer** sulla proprietà [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) dell'oggetto [PaintEventArgs.](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1)

 

[**L'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) può memorizzare temporaneamente nella cache i dati dell'input penna. Per usare questa funzionalità nel codice gestito, impostare la [proprietà EnableDataCache](/previous-versions/ms826349(v=msdn.10)) su **TRUE.** Quando l'oggetto [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) riceve una chiamata al relativo metodo [**IStylusSyncPlugin.StylusUp,**](/previous-versions/ms826366(v=msdn.10)) memorizza nella cache i dati del tratto e aggiunge dati dello stilo personalizzati alla coda input in risposta all'oggetto [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) per il tratto. La proprietà [CustomDataId](/previous-versions/ms824749(v=msdn.10)) dell'oggetto [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) è impostata sul valore [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) e la proprietà Data dell'oggetto **CustomStylusData** contiene un oggetto DynamicRendererCachedData. Chiamare il metodo [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) dell'oggetto **DynamicRenderer** dopo che il tratto è stato raccolto e può essere sottoposto a rendering in modo statico. Quando il [**metodo Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) viene chiamato mentre l'oggetto **DynamicRenderer** è abilitato, l'oggetto **DynamicRenderer** ridisegna tutti i tratti memorizzati nella cache. Quando la [**proprietà DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) è impostata su **false,** i dati del tratto memorizzati nella cache vengono eliminati.

Il diagramma seguente illustra come [**l'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) aggiunge dati ai dati della penna del tablet quando viene impostata la proprietà [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) dell'oggetto **DynamicRenderer.**

![Figura che mostra il flusso di dati dynamicrenderer](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

In questo diagramma il cerchio con lettera "SD" rappresenta un oggetto [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) e i cerchi con lettera "P" rappresentano gli oggetti [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. Il cerchio con lettera "SU" rappresenta un [**oggetto StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) che l'oggetto **RealTimeStylus** sta elaborando. Viene inviato alla raccolta di plug-in sincroni e quindi inserito nella coda di output. I cerchi con lettera "DR" rappresentano i dati dello stilo personalizzati aggiunti alla coda di input dal plug-in [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) in risposta alla notifica dello stilo verso l'alto associata a "SU". I dati dello stilo personalizzati con lettera "DR" vengono quindi passati ai plug-in sincroni e quindi alla coda di output prima che vengano elaborati i dati della penna del tablet successivi. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet. Nel diagramma è rappresentato anche il plug-in ink-collector che chiama il metodo [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) dell'oggetto **DynamicRenderer** per rilasciare i dati del tratto memorizzati nella cache dopo che il plug-in ink-collection ha elaborato il tratto.

### <a name="special-considerations"></a>Considerazioni speciali

L'elenco seguente descrive altri punti da considerare quando si usa [**l'oggetto DynamicRenderer.**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))

-   Non associare un [**oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a più [**oggetti RealTimeStylus.**](realtimestylus-class.md) Dopo aver **abilitato due oggetti RealTimeStylus** a cui è collegato l'oggetto **DynamicRenderer,** si verifica quanto segue.

    -   [**L'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) genera un'eccezione in risposta alla seconda chiamata al metodo [**RealTimeStylusEnabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled)
    -   Il secondo [**oggetto RealTimeStylus**](realtimestylus-class.md) abilitato genera un oggetto [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) e notifica l'errore ai plug-in rimanenti nelle raccolte di plug-in.
    -   [**L'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) interrompe il rendering dei dati della penna del tablet.

-   L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione quando viene chiamato il metodo [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) con il *parametro guid* impostato sull'identificatore univoco globale (GUID) DynamicRendererCachedDataGuid.
-   [**L'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) viene implementato come wrapper Component Object Model (COM) e non è possibile chiamare direttamente i relativi metodi di interfaccia [**IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) Per altre informazioni sull'operazione COM e [**sull'oggetto RealTimeStylus,**](realtimestylus-class.md) vedere Note sull'implementazione [per le API StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Rendering personalizzato

È possibile creare un plug-in renderer dinamico creando un plug-in sincrono che sottoscrive le notifiche [**StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) Il plug-in può quindi eseguire il rendering del tratto mentre viene disegnato. Può trattarsi di un modo per implementare uno strumento di selezione che usa ad esempio una casella di selezione o una selezione in formato libero.

 

 
