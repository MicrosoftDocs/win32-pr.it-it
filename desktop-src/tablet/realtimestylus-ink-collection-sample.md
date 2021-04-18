---
description: Questa applicazione illustra il rendering e la raccolta di input penna quando si usa la classe RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Esempio di raccolta inchiostro RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315557"
---
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="bc7bc-103">Esempio di raccolta inchiostro RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="bc7bc-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="bc7bc-104">Questa applicazione illustra il rendering e la raccolta di input penna quando si usa la classe [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="bc7bc-105">Progetto InkCollection</span><span class="sxs-lookup"><span data-stu-id="bc7bc-105">The InkCollection Project</span></span>

<span data-ttu-id="bc7bc-106">Questo esempio è costituito da una singola soluzione che contiene un progetto, InkCollection.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="bc7bc-107">L'applicazione definisce lo `InkCollection` spazio dei nomi che contiene una singola classe, denominata anche `InkCollection` .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="bc7bc-108">La classe eredita dalla classe del [form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa l'interfaccia [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="bc7bc-109">La classe InkCollection definisce un set di costanti private utilizzate per specificare diversi spessori di input penna.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="bc7bc-110">La classe dichiara anche istanze private della classe [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , la classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` e la classe [renderer](/previous-versions/ms828481(v=msdn.10)) `myRenderer` .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="bc7bc-111">**DynamicRenderer** esegue il rendering del [tratto](/previous-versions/ms552692(v=vs.100)) attualmente in fase di raccolta.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="bc7bc-112">L'oggetto Renderer, `myRenderer` , esegue il rendering degli oggetti Stroke che sono già stati raccolti.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="bc7bc-113">La classe dichiara anche un oggetto [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , usato per archiviare i dati dei pacchetti raccolti da uno o più oggetti [Cursor](/previous-versions/ms552104(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="bc7bc-114">I valori [ID](/previous-versions/ms824826(v=msdn.10)) dell'oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) vengono utilizzati come chiave Hashtable per identificare in modo univoco i dati dei pacchetti raccolti per un determinato oggetto cursore.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="bc7bc-115">Un'istanza privata dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) , `myInk` , archivia gli oggetti [Stroke](/previous-versions/ms552692(v=vs.100)) raccolti da `myRealTimeStylus` .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="bc7bc-116">Evento di caricamento del form</span><span class="sxs-lookup"><span data-stu-id="bc7bc-116">The Form Load Event</span></span>

<span data-ttu-id="bc7bc-117">Nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) per il form, `myDynamicRenderer` viene creata un'istanza di tramite l'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) che accetta un controllo come argomento e `myRenderer` viene costruito con un costruttore senza argomenti.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="bc7bc-118">Prestare attenzione al commento che segue la creazione di un'istanza dei renderer, perché `myDynamicRenderer` utilizza i valori predefiniti per [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) durante il rendering dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="bc7bc-119">Si tratta di un comportamento standard.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-119">This is standard behavior.</span></span> <span data-ttu-id="bc7bc-120">Tuttavia, se si desidera assegnare al rendering dell'input penna `myDynamicRenderer` un aspetto diverso da quello di input penna eseguito da `myRenderer` , è possibile modificare la proprietà [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) in `myDynamicRenderer` .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="bc7bc-121">A tale scopo, rimuovere il commento dalle righe seguenti prima di compilare ed eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="bc7bc-122">Successivamente, l'applicazione crea l'oggetto [**RealTimeStylus**](realtimestylus-class.md) usato per ricevere le notifiche dello stilo e aggiunge l'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) alla coda di notifiche del plug-in sincrono.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="bc7bc-123">In particolare, `myRealTimeStylus` aggiunge `myDynamicRenderer` alla proprietà [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="bc7bc-124">Il modulo viene quindi aggiunto alla coda di notifiche del plug-in asincrono.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="bc7bc-125">In particolare, `InkCollection` viene aggiunto alla proprietà [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="bc7bc-126">Infine, `myRealTimeStylus` e `myDynamicRenderer` sono abilitati e vengono create istanze di pacchetti e myInk.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="bc7bc-127">Oltre ad associare i gestori dei menu per modificare il colore e le dimensioni dell'input penna, prima di implementare l'interfaccia è necessario un blocco di codice più breve.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="bc7bc-128">L'esempio deve gestire l'evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del modulo.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="bc7bc-129">Nel gestore eventi, l'applicazione deve essere aggiornata `myDynamicRenderer` perché è possibile che un oggetto [Stroke](/previous-versions/ms552692(v=vs.100)) venga raccolto nel momento in cui si verifica l'evento Paint.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="bc7bc-130">In tal caso, è necessario ridisegnare la porzione dell'oggetto Stroke che è già stato raccolto.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="bc7bc-131">Il [renderer](/previous-versions/ms828481(v=msdn.10)) statico viene usato per ridisegnare gli oggetti Stroke che sono già stati raccolti.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="bc7bc-132">Questi tratti si trovano nell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) perché vengono inseriti quando vengono disegnati, come illustrato nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="bc7bc-133">Implementazione dell'interfaccia IStylusAsyncPlugin</span><span class="sxs-lookup"><span data-stu-id="bc7bc-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="bc7bc-134">L'applicazione di esempio definisce i tipi di notifiche che è interessato a ricevere nell'implementazione della proprietà [DataInterest](/previous-versions/ms824769(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="bc7bc-135">La proprietà DataInterest definisce quindi le notifiche che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) trasmette al form.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="bc7bc-136">Per questo esempio, la proprietà DataInterest definisce l'interesse per le notifiche **StylusDown**, **packets**, **StylusUp** e **Error** tramite l'enumerazione [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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
```



<span data-ttu-id="bc7bc-137">La notifica [StylusDown](/previous-versions/ms824779(v=msdn.10)) si verifica quando la penna tocca la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="bc7bc-138">In questo caso, l'esempio alloca una matrice usata per archiviare i dati dei pacchetti per l'oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="bc7bc-139">Il [StylusDownData](/previous-versions/ms824107(v=msdn.10)) dal metodo StylusDown viene aggiunto alla matrice e la matrice viene inserita nella tabella hash usando la proprietà [ID](/previous-versions/ms824826(v=msdn.10)) dell'oggetto stilo come chiave.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="bc7bc-140">La notifica dei [pacchetti](/previous-versions/ms824773(v=msdn.10)) si verifica quando la penna si sposta sulla superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="bc7bc-141">Quando si verifica questa situazione, l'applicazione aggiunge nuovi [StylusDownData](/previous-versions/ms824107(v=msdn.10)) nella matrice di pacchetti per l'oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="bc7bc-142">Questa operazione viene eseguita usando la proprietà [ID](/previous-versions/ms824826(v=msdn.10)) dell'oggetto stilo come chiave per recuperare la matrice di pacchetti per lo stilo dalla tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="bc7bc-143">I nuovi dati del pacchetto vengono quindi inseriti nella matrice recuperata.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="bc7bc-144">La notifica [StylusUp](/previous-versions/ms824782(v=msdn.10)) si verifica quando la penna lascia la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="bc7bc-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="bc7bc-145">Quando si verifica questa notifica, nell'esempio viene recuperata la matrice di pacchetti per questo oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) dalla tabella hash che viene rimossa dalla tabella hash perché non è più necessaria, viene aggiunto nei nuovi dati del pacchetto e viene utilizzata la matrice di dati del pacchetto per creare un nuovo oggetto [Stroke](/previous-versions/ms552692(v=vs.100)) `stroke` .</span><span class="sxs-lookup"><span data-stu-id="bc7bc-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



<span data-ttu-id="bc7bc-146">Per un esempio in cui viene illustrato un uso più affidabile della classe [**RealTimeStylus**](realtimestylus-class.md) , incluso l'uso della creazione di plug-in personalizzati, vedere [esempio di plug-in RealTimeStylus](realtimestylus-plug-in-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bc7bc-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc7bc-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc7bc-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc7bc-148">[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="bc7bc-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="bc7bc-149">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bc7bc-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="bc7bc-150">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bc7bc-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="bc7bc-151">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bc7bc-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="bc7bc-152">Accesso e modifica dell'input dello stilo</span><span class="sxs-lookup"><span data-stu-id="bc7bc-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
