---
description: L'oggetto RealTimeStylus è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del tablet.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-in e classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc522eb6f73b384d0c2c1846edb2b20cdcb89d34ef42633b08ca865950c8ce16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843381"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-in e classe RealTimeStylus

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del tablet. I plug-in, oggetti che implementano [**l'interfaccia IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) possono essere aggiunti a un **oggetto RealTimeStylus.** I plug-in sincroni vengono in genere chiamati direttamente dall'oggetto **RealTimeStylus** in un thread ad alta priorità, mentre i plug-in asincroni vengono in genere chiamati sul thread dell'interfaccia utente dell'applicazione. Creare o usare plug-in sincroni per attività che richiedono l'accesso in tempo reale al flusso di dati e non vengono eseguite dal punto di vista del calcolo, ad esempio il filtro dei pacchetti. Creare o usare plug-in asincroni per attività che non richiedono l'accesso in tempo reale al flusso di dati, ad esempio la raccolta di input penna.

Alcune attività possono essere impegnative dal punto di vista del calcolo ma richiedono l'accesso in tempo reale al flusso di dati, ad esempio il riconoscimento dei movimenti a più sequenze. Per soddisfare queste esigenze, le API StylusInput forniscono un modello [**RealTimeStylus**](realtimestylus-class.md) a catena che consente di usare due **oggetti RealTimeStylus,** ognuno in esecuzione nel proprio thread. Per altre informazioni sul modello **RealTimeStylus** a catena, vedere [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

Entrambe [**le interfacce IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definiscono gli stessi metodi. Questi metodi consentono all'oggetto [**RealTimeStylus**](realtimestylus-class.md) di passare i dati della penna a ogni plug-in, indipendentemente dal fatto che si tratta di un plug-in asincrono o sincrono. Le proprietà [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) e [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) consentono a ogni plug-in di sottoscrivere dati specifici nel flusso di dati della penna del tablet. Un plug-in deve sottoscrivere solo i dati necessari per eseguire l'attività, riducendo al minimo le richieste di prestazioni. Per altre informazioni sul threading e **sulla classe RealTimeStylus,** vedere Considerazioni sul [threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) usa oggetti nello spazio dei nomi [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) per passare i dati della penna ai relativi plug-in. **RealTimeStylus** intercetta anche le eccezioni generate dai plug-in. Quando **RealTimeStylus** rileva le eccezioni, invia una notifica ai plug-in chiamando il metodo [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [IStylusAsyncPlugin.Error.](/previous-versions/ms824771(v=msdn.10)) Per altre informazioni sull'uso dei dati [plug-in, vedere Dati plug-in e la classe RealTimeStylus.](plug-in-data-and-the-realtimestylus-class.md) Per altre informazioni sulla gestione degli errori, vedere Considerazioni sulla gestione degli errori per le [API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) e la sezione Dati degli errori dei dati del plug-in e della classe RealTimeStylus.

> [!Note]  
> È necessario collegare almeno un plug-in [**all'oggetto RealTimeStylus**](realtimestylus-class.md) prima che l'oggetto **RealTimeStylus** possa essere abilitato.

 

Negli argomenti seguenti vengono descritte alcune categorie comuni di plug-in.

-   [Plug-in raccolta input penna](ink-collection-plug-ins.md)
-   [Plug-in renderer dinamici](dynamic-renderer-plug-ins.md)
-   [Plug-in recognizer](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Considerazioni speciali

A causa della natura complessa [**dell'oggetto RealTimeStylus,**](realtimestylus-class.md) è necessario tenere presente quanto segue.

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in modifica la raccolta di plug-in a cui è collegato. Ciò si verifica solo quando il plug-in esegue questa operazione mentre viene chiamato dall'oggetto **RealTimeStylus** come membro di tale raccolta.

L'esempio C seguente è il codice che causa la generazione di un'eccezione da parte \# dell'oggetto [**RealTimeStylus.**](realtimestylus-class.md)


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



[**L'oggetto RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in chiama il metodo [Dispose](/previous-versions/ms825891(v=msdn.10)) dell'oggetto **RealTimeStylus.** Ciò si verifica solo quando il plug-in esegue questa operazione mentre viene chiamato **dall'oggetto RealTimeStylus.**

L'esempio C seguente è il codice che causa la generazione di un'eccezione da parte \# dell'oggetto [**RealTimeStylus.**](realtimestylus-class.md)


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



Le raccolte di plug-in possono essere modificate mentre [**l'oggetto RealTimeStylus**](realtimestylus-class.md) è abilitato. Tuttavia, ciò può rendere il comportamento dell'applicazione più difficile da prevedere. Quando viene aggiunto un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) o [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) del plug-in. Quando un plug-in viene rimosso mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) o [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) del plug-in. Ciò consente al plug-in di mantenere lo stato corretto senza dover controllare la [proprietà Enabled](/previous-versions/ms824832(v=msdn.10)) dell'oggetto **RealTimeStylus.**

Quando un plug-in viene aggiunto mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non contenere informazioni sufficienti per stabilire in modo adeguato il contesto dei dati iniziali. Ad esempio, il plug-in appena aggiunto potrebbe iniziare a ricevere i dati del pacchetto da una penna a metà corsa. Analogamente, quando un plug-in viene rimosso mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non essere sufficienti per completare l'elaborazione dei dati.

> [!Note]  
> Per la stabilità complessiva, reimpostare lo stato interno di un plug-in quando viene chiamato il metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello RealTimeStylus a catena](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considerazioni sulla gestione degli errori per le API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considerazioni sul threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
