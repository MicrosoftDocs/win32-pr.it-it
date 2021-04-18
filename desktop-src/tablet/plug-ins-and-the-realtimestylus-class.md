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
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="e045d-103">Plug-in e classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e045d-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="e045d-104">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e045d-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="e045d-105">I plug-in, ovvero gli oggetti che implementano l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , possono essere aggiunti a un oggetto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="e045d-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="e045d-106">I plug-in sincroni vengono generalmente chiamati direttamente dall'oggetto **RealTimeStylus** su un thread ad alta priorità, mentre i plug-in asincroni vengono in genere chiamati sul thread dell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e045d-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="e045d-107">Creare o usare plug-in sincroni per le attività che richiedono l'accesso in tempo reale al flusso di dati e non richiedono un calcolo, ad esempio il filtro dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e045d-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="e045d-108">Creare o usare plug-in asincroni per le attività che non richiedono l'accesso in tempo reale al flusso di dati, ad esempio la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="e045d-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="e045d-109">Alcune attività possono essere richieste dal punto di vista del calcolo, ma richiedono l'accesso in tempo reale al flusso di dati, ad esempio il riconoscimento di movimenti a più sequenze.</span><span class="sxs-lookup"><span data-stu-id="e045d-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="e045d-110">Per soddisfare queste esigenze, le API StylusInput forniscono un modello [**RealTimeStylus**](realtimestylus-class.md) a cascata che consente di usare due oggetti **RealTimeStylus** , ognuno in esecuzione sul proprio thread.</span><span class="sxs-lookup"><span data-stu-id="e045d-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="e045d-111">Per ulteriori informazioni sul modello **RealTimeStylus** a cascata, vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="e045d-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="e045d-112">Entrambe le interfacce [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definiscono gli stessi metodi.</span><span class="sxs-lookup"><span data-stu-id="e045d-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="e045d-113">Questi metodi consentono all'oggetto [**RealTimeStylus**](realtimestylus-class.md) di passare i dati della penna a ogni plug-in, indipendentemente dal fatto che si tratti di un plug-in asincrono o sincrono.</span><span class="sxs-lookup"><span data-stu-id="e045d-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="e045d-114">Le proprietà [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) e [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) consentono a ogni plug-in di sottoscrivere dati specifici nel flusso di dati della penna del tablet.</span><span class="sxs-lookup"><span data-stu-id="e045d-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="e045d-115">Un plug-in deve sottoscrivere solo i dati necessari per eseguire l'attività, riducendo al minimo le esigenze di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e045d-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="e045d-116">Per ulteriori informazioni sul threading e sulla classe **RealTimeStylus** , vedere [considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="e045d-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="e045d-117">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) usa gli oggetti nello spazio dei nomi [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) per passare i dati della penna ai relativi plug-in. Il metodo **RealTimeStylus** intercetta anche le eccezioni generate dai plug-in. Quando **RealTimeStylus** rileva le eccezioni, invia una notifica ai plug-in chiamando il metodo [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) o [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="e045d-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="e045d-118">Per ulteriori informazioni sull'utilizzo dei dati plug-in, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e045d-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="e045d-119">Per ulteriori informazioni sulla gestione degli errori, vedere [considerazioni sulla gestione degli errori per le API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) e la sezione relativa ai dati degli errori dei dati plug-in e della classe RealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="e045d-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="e045d-120">Almeno un plug-in deve essere collegato all'oggetto [**RealTimeStylus**](realtimestylus-class.md) prima che l'oggetto **RealTimeStylus** possa essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="e045d-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="e045d-121">Negli argomenti seguenti vengono descritte alcune categorie comuni di plug-in.</span><span class="sxs-lookup"><span data-stu-id="e045d-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="e045d-122">Plug-in per la raccolta di input penna</span><span class="sxs-lookup"><span data-stu-id="e045d-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="e045d-123">Plug-in di renderer dinamici</span><span class="sxs-lookup"><span data-stu-id="e045d-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="e045d-124">Plug-in di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="e045d-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="e045d-125">Considerazioni speciali</span><span class="sxs-lookup"><span data-stu-id="e045d-125">Special Considerations</span></span>

<span data-ttu-id="e045d-126">A causa della natura complessa dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) , è necessario tenere presente quanto segue.</span><span class="sxs-lookup"><span data-stu-id="e045d-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="e045d-127">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in modifica la raccolta di plug-in a cui è collegata.</span><span class="sxs-lookup"><span data-stu-id="e045d-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="e045d-128">Questa situazione si verifica solo quando il plug-in lo fa mentre viene chiamato dall'oggetto **RealTimeStylus** come membro di tale raccolta.</span><span class="sxs-lookup"><span data-stu-id="e045d-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="e045d-129">Nell'esempio C riportato \# di seguito viene utilizzato il codice che determina la generazione di un'eccezione da parte dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e045d-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="e045d-130">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in chiama il metodo [Dispose](/previous-versions/ms825891(v=msdn.10)) dell'oggetto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="e045d-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="e045d-131">Questa situazione si verifica solo quando il plug-in lo fa mentre viene chiamato dall'oggetto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="e045d-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="e045d-132">Nell'esempio C riportato \# di seguito viene utilizzato il codice che determina la generazione di un'eccezione da parte dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e045d-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="e045d-133">È possibile modificare le raccolte di plug-in mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato; Questo può tuttavia rendere più difficile la stima del comportamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e045d-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="e045d-134">Quando si aggiunge un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo IStylusAsyncPlugin. [RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) del plug-in.</span><span class="sxs-lookup"><span data-stu-id="e045d-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="e045d-135">Quando si rimuove un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo IStylusAsyncPlugin. [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) del plug-in.</span><span class="sxs-lookup"><span data-stu-id="e045d-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="e045d-136">In questo modo il plug-in è in grado di mantenere lo stato appropriato senza dover controllare la proprietà [Enabled](/previous-versions/ms824832(v=msdn.10)) dell'oggetto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="e045d-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="e045d-137">Quando si aggiunge un plug-in mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non contenere informazioni sufficienti per stabilire adeguatamente il contesto dei dati iniziali.</span><span class="sxs-lookup"><span data-stu-id="e045d-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="e045d-138">Ad esempio, il plug-in appena aggiunto potrebbe iniziare a ricevere i dati dei pacchetti da una penna a metà tratto.</span><span class="sxs-lookup"><span data-stu-id="e045d-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="e045d-139">Analogamente, quando un plug-in è stato rimosso mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non essere sufficienti per completare l'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="e045d-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="e045d-140">Per la stabilità complessiva, reimpostare lo stato interno di un plug-in quando viene chiamato il metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .</span><span class="sxs-lookup"><span data-stu-id="e045d-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e045d-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e045d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e045d-142">Modello di RealTimeStylus a cascata</span><span class="sxs-lookup"><span data-stu-id="e045d-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="e045d-143">Considerazioni sulla gestione degli errori per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="e045d-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="e045d-144">Dati plug-in e classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="e045d-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="e045d-145">Considerazioni relative al threading per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="e045d-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
