---
description: Questa applicazione illustra l'uso della classe RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Esempio di plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234079"
---
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="6c1ce-103">Esempio di plug-in RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="6c1ce-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="6c1ce-104">Questa applicazione illustra l'uso della classe [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="6c1ce-105">Per una panoramica dettagliata delle API StylusInput, inclusa la classe **RealTimeStylus** , vedere [accesso e manipolazione dell'input dello stilo](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="6c1ce-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="6c1ce-106">Per informazioni sui plug-in sincroni e asincroni, vedere [plug-in e la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="6c1ce-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="6c1ce-107">Panoramica dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6c1ce-107">Overview of the Sample</span></span>

<span data-ttu-id="6c1ce-108">I plug-in, ovvero gli oggetti che implementano l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , possono essere aggiunti a un oggetto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="6c1ce-109">Questa applicazione di esempio usa diversi tipi di plug-in:</span><span class="sxs-lookup"><span data-stu-id="6c1ce-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="6c1ce-110">Plug-in del filtro pacchetti: modifica i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="6c1ce-111">Il plug-in filtro pacchetti in questo esempio modifica le informazioni sui pacchetti vincolando tutti i dati dei pacchetti (x, y) in un'area rettangolare.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="6c1ce-112">Plug-in di renderer dinamico personalizzato: modifica le qualità del rendering dinamico.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="6c1ce-113">Il plug-in per il rendering dinamico personalizzato in questo esempio modifica il modo in cui viene eseguito il rendering dell'input penna disegnando un piccolo cerchio intorno a ogni punto (x, y) in un tratto.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="6c1ce-114">Plug-in di renderer dinamico: modifica le qualità del rendering dinamico.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="6c1ce-115">In questo esempio viene illustrato l'utilizzo dell'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) come plug-in per gestire il rendering dinamico dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="6c1ce-116">Plug-in di riconoscimento movimento: riconosce i movimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="6c1ce-117">In questo esempio viene illustrato l'utilizzo dell'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) come plug-in per riconoscere i movimenti dell'applicazione (quando in esecuzione in un sistema con il riconoscitore di movimento Microsoft presente).</span><span class="sxs-lookup"><span data-stu-id="6c1ce-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="6c1ce-118">Inoltre, in questo esempio viene fornita un'interfaccia utente che consente all'utente di aggiungere, rimuovere e modificare l'ordine di ciascun plug-in nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="6c1ce-119">La soluzione di esempio contiene due progetti, RealTimeStylusPluginApp e RealTimeStylusPlugins.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="6c1ce-120">RealTimeStylusPluginApp contiene l'interfaccia utente per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="6c1ce-121">RealTimeStylusPlugins contiene le implementazioni dei plug-in. Il progetto RealTimeStylusPlugins definisce lo spazio dei nomi RealTimeStylusPlugins, che contiene i plug-in di filtro pacchetti e renderer dinamici personalizzati. Il progetto RealTimeStylusPluginApp fa riferimento a questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="6c1ce-122">Il progetto RealTimeStylusPlugins usa gli spazi dei nomi [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="6c1ce-123">Per una panoramica degli spazi dei nomi [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) e [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , vedere [architettura delle API StylusInput](architecture-of-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="6c1ce-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="6c1ce-124">Plug-in del filtro pacchetti</span><span class="sxs-lookup"><span data-stu-id="6c1ce-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="6c1ce-125">Il plug-in del filtro pacchetti è un plug-in sincrono che illustra la modifica dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="6c1ce-126">In particolare, definisce un rettangolo nel form.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="6c1ce-127">Viene eseguito il rendering di tutti i pacchetti disegnati all'esterno dell'area all'interno dell'area.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="6c1ce-128">La classe plug-in, `PacketFilterPlugin` , registra per la notifica `StylusDown` degli `StylusUp` eventi di `Packets` input penna, e.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="6c1ce-129">La classe implementa i metodi [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))e [packets](/previous-versions/ms824756(v=msdn.10)) definiti nella classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="6c1ce-130">Il costruttore pubblico per `PacketFilterPlugin` richiede una struttura [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="6c1ce-131">Questo rettangolo definisce l'area rettangolare, in coordinate dello spazio input penna (. 01mm = 1 unità HIMETRIC), in cui saranno contenuti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="6c1ce-132">Il rettangolo viene mantenuto in un campo privato, `rectangle` .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-132">The rectangle is held in a private field, `rectangle`.</span></span>


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



<span data-ttu-id="6c1ce-133">La `PacketFilterPlugin` classe esegue la registrazione per le notifiche degli eventi implementando la funzione di accesso get per la proprietà [DataInterest](/previous-versions/ms824752(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="6c1ce-134">In questo caso, il plug-in è interessato a rispondere alle `StylusDown` notifiche, `Packets` , `StylusUp` e `Error` .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="6c1ce-135">L'esempio restituisce questi valori come definito nell'enumerazione [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="6c1ce-136">Il metodo [StylusDown](/previous-versions/ms824761(v=msdn.10)) viene chiamato quando la penna suggerimento Contatta la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="6c1ce-137">Il metodo [StylusUp](/previous-versions/ms824764(v=msdn.10)) viene chiamato quando la penna suggerimento lascia la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="6c1ce-138">Il metodo [packets](/previous-versions/ms824756(v=msdn.10)) viene chiamato quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md) riceve i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="6c1ce-139">Il metodo [Error](/previous-versions/ms585069(v=vs.100)) viene chiamato quando il plug-in corrente o un plug-in precedente genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



<span data-ttu-id="6c1ce-140">La `PacketFilterPlugin` classe gestisce la maggior parte di queste notifiche in un metodo helper, `ModifyPacketData` .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="6c1ce-141">Il `ModifyPacketData` metodo ottiene i valori x e y per ogni nuovo pacchetto dalla classe [PacketsData](/previous-versions/ms824590(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="6c1ce-142">Se uno dei due valori è esterno al rettangolo, il metodo sostituisce il valore con il punto più vicino che ancora rientra nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="6c1ce-143">Di seguito è riportato un esempio di come un plug-in può sostituire i dati del pacchetto così come vengono ricevuti dal flusso di input penna.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="6c1ce-144">Plug-in renderer dinamico personalizzato</span><span class="sxs-lookup"><span data-stu-id="6c1ce-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="6c1ce-145">La `CustomDynamicRenderer` classe implementa inoltre la classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) per ricevere le notifiche di input penna.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="6c1ce-146">Gestisce quindi la `Packets` notifica per creare un piccolo cerchio intorno a ogni nuovo punto di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="6c1ce-147">La classe contiene una variabile [grafica](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) che contiene un riferimento all'oggetto Graphics passato nel costruttore della classe.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="6c1ce-148">Si tratta dell'oggetto Graphics usato per il rendering dinamico.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="6c1ce-149">Quando il plug-in renderer dinamico personalizzato riceve una notifica di pacchetti, estrae i dati (x, y) e disegna un piccolo cerchio verde intorno al punto.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="6c1ce-150">Questo è un esempio di rendering personalizzato basato sul flusso di input penna.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-150">This is an example of custom rendering based on the pen-input stream.</span></span>


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="6c1ce-151">Progetto RealTimeStylusPluginApp</span><span class="sxs-lookup"><span data-stu-id="6c1ce-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="6c1ce-152">Il progetto RealTimeStylusPluginApp illustra i plug-in descritti in precedenza, nonché i plug-in [**GestureRecognizer**](gesturerecognizer-class.md) e [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . L'interfaccia utente del progetto è costituita da:</span><span class="sxs-lookup"><span data-stu-id="6c1ce-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="6c1ce-153">Form che contiene un controllo [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) utilizzato per definire l'area di immissione dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="6c1ce-154">Controllo [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) per elencare e selezionare i plug-in disponibili.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="6c1ce-155">Coppia di [oggetti Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) che consente di riordinare i plug-in.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="6c1ce-156">Il progetto definisce una struttura, `PlugInListItem` , per semplificare la gestione dei plug-in utilizzati nel progetto.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="6c1ce-157">La `PlugInListItem` struttura contiene il plug-in e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="6c1ce-158">La `RealTimeStylusPluginApp` classe stessa implementa la classe [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="6c1ce-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="6c1ce-159">Questa operazione è necessaria in modo che la `RealTimeStylusPluginApp` classe possa ricevere una notifica quando il plug-in [**GestureRecognizer**](gesturerecognizer-class.md) aggiunge dati di movimento alla coda di output.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="6c1ce-160">L'applicazione esegue la registrazione per la notifica di [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="6c1ce-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="6c1ce-161">Quando vengono ricevuti i dati di movimento, `RealTimeStylusPluginApp` ne inserisce una descrizione sulla barra di stato nella parte inferiore del modulo.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> Nell'implementazione di [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) è interessante identificare i dati dei movimenti personalizzati nella coda di output in base al GUID (usando il campo [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) o in base al tipo (usando il risultato dell'istruzione As). Nell'esempio vengono utilizzate entrambe le tecniche di identificazione a scopo dimostrativo. <span data-ttu-id="6c1ce-164">È valido anche uno solo degli approcci.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="6c1ce-165">Nel gestore dell'evento Load del form, l'applicazione crea istanze delle `PacketFilter` classi e `CustomDynamicRenderer` e le aggiunge alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="6c1ce-166">L'applicazione tenta quindi di creare un'istanza della classe [**GestureRecognizer**](gesturerecognizer-class.md) e, in caso di esito positivo, la aggiunge alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="6c1ce-167">Questa operazione ha esito negativo se il riconoscitore di movimento non è presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="6c1ce-168">Successivamente, l'applicazione crea un'istanza di un oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e la aggiunge alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="6c1ce-169">Infine, l'applicazione Abilita tutti i plug-in e l'oggetto [**RealTimeStylus**](realtimestylus-class.md) stesso.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="6c1ce-170">Un altro aspetto importante da considerare sull'esempio è che nei metodi helper l'oggetto [**RealTimeStylus**](realtimestylus-class.md) viene prima disabilitato prima che i plug-in vengano aggiunti o rimossi e quindi riabilitati dopo il completamento dell'aggiunta o della rimozione.</span><span class="sxs-lookup"><span data-stu-id="6c1ce-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a><span data-ttu-id="6c1ce-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c1ce-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6c1ce-172">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="6c1ce-173">[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="6c1ce-174">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="6c1ce-175">[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="6c1ce-176">[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="6c1ce-177">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="6c1ce-178">[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6c1ce-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="6c1ce-179">Accesso e modifica dell'input dello stilo</span><span class="sxs-lookup"><span data-stu-id="6c1ce-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="6c1ce-180">Plug-in e classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="6c1ce-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="6c1ce-181">Esempio di raccolta inchiostro RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="6c1ce-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
