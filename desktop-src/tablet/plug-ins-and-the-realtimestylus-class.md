---
description: L'oggetto RealTimeStylus è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del Tablet PC.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-in e classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318693"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-in e classe RealTimeStylus

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del Tablet PC. I plug-in, ovvero gli oggetti che implementano l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , possono essere aggiunti a un oggetto **RealTimeStylus** . I plug-in sincroni vengono generalmente chiamati direttamente dall'oggetto **RealTimeStylus** su un thread ad alta priorità, mentre i plug-in asincroni vengono in genere chiamati sul thread dell'interfaccia utente dell'applicazione. Creare o usare plug-in sincroni per le attività che richiedono l'accesso in tempo reale al flusso di dati e non richiedono un calcolo, ad esempio il filtro dei pacchetti. Creare o usare plug-in asincroni per le attività che non richiedono l'accesso in tempo reale al flusso di dati, ad esempio la raccolta di input penna.

Alcune attività possono essere richieste dal punto di vista del calcolo, ma richiedono l'accesso in tempo reale al flusso di dati, ad esempio il riconoscimento di movimenti a più sequenze. Per soddisfare queste esigenze, le API StylusInput forniscono un modello [**RealTimeStylus**](realtimestylus-class.md) a cascata che consente di usare due oggetti **RealTimeStylus** , ognuno in esecuzione sul proprio thread. Per ulteriori informazioni sul modello **RealTimeStylus** a cascata, vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).

Entrambe le interfacce [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definiscono gli stessi metodi. Questi metodi consentono all'oggetto [**RealTimeStylus**](realtimestylus-class.md) di passare i dati della penna a ogni plug-in, indipendentemente dal fatto che si tratti di un plug-in asincrono o sincrono. Le proprietà [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) e [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) consentono a ogni plug-in di sottoscrivere dati specifici nel flusso di dati della penna del tablet. Un plug-in deve sottoscrivere solo i dati necessari per eseguire l'attività, riducendo al minimo le esigenze di prestazioni. Per ulteriori informazioni sul threading e sulla classe **RealTimeStylus** , vedere [considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) usa gli oggetti nello spazio dei nomi [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) per passare i dati della penna ai relativi plug-in. Il metodo **RealTimeStylus** intercetta anche le eccezioni generate dai plug-in. Quando **RealTimeStylus** rileva le eccezioni, invia una notifica ai plug-in chiamando il metodo [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) o [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) . Per ulteriori informazioni sull'utilizzo dei dati plug-in, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) . Per ulteriori informazioni sulla gestione degli errori, vedere [considerazioni sulla gestione degli errori per le API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) e la sezione relativa ai dati degli errori dei dati plug-in e della classe RealTimeStylus.

> [!Note]  
> Almeno un plug-in deve essere collegato all'oggetto [**RealTimeStylus**](realtimestylus-class.md) prima che l'oggetto **RealTimeStylus** possa essere abilitato.

 

Negli argomenti seguenti vengono descritte alcune categorie comuni di plug-in.

-   [Plug-in per la raccolta di input penna](ink-collection-plug-ins.md)
-   [Plug-in di renderer dinamici](dynamic-renderer-plug-ins.md)
-   [Plug-in di riconoscimento](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Considerazioni speciali

A causa della natura complessa dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) , è necessario tenere presente quanto segue.

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in modifica la raccolta di plug-in a cui è collegata. Questa situazione si verifica solo quando il plug-in lo fa mentre viene chiamato dall'oggetto **RealTimeStylus** come membro di tale raccolta.

Nell'esempio C riportato \# di seguito viene utilizzato il codice che determina la generazione di un'eccezione da parte dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) .


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in chiama il metodo [Dispose](/previous-versions/ms825891(v=msdn.10)) dell'oggetto **RealTimeStylus** . Questa situazione si verifica solo quando il plug-in lo fa mentre viene chiamato dall'oggetto **RealTimeStylus** .

Nell'esempio C riportato \# di seguito viene utilizzato il codice che determina la generazione di un'eccezione da parte dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) .


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



È possibile modificare le raccolte di plug-in mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato; Questo può tuttavia rendere più difficile la stima del comportamento dell'applicazione. Quando si aggiunge un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo IStylusAsyncPlugin. [RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) del plug-in. Quando si rimuove un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo IStylusAsyncPlugin. [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) del plug-in. In questo modo il plug-in è in grado di mantenere lo stato appropriato senza dover controllare la proprietà [Enabled](/previous-versions/ms824832(v=msdn.10)) dell'oggetto **RealTimeStylus** .

Quando si aggiunge un plug-in mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non contenere informazioni sufficienti per stabilire adeguatamente il contesto dei dati iniziali. Ad esempio, il plug-in appena aggiunto potrebbe iniziare a ricevere i dati dei pacchetti da una penna a metà tratto. Analogamente, quando un plug-in è stato rimosso mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non essere sufficienti per completare l'elaborazione dei dati.

> [!Note]  
> Per la stabilità complessiva, reimpostare lo stato interno di un plug-in quando viene chiamato il metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considerazioni sulla gestione degli errori per le API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
