---
description: Di seguito sono riportate alcune considerazioni relative al threading di Tablet PC per la libreria gestita.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considerazioni sul threading della libreria gestita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314910"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="3396e-103">Considerazioni sul threading della libreria gestita</span><span class="sxs-lookup"><span data-stu-id="3396e-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="3396e-104">Di seguito sono riportate alcune considerazioni relative al threading di Tablet PC per la libreria gestita.</span><span class="sxs-lookup"><span data-stu-id="3396e-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="3396e-105">Thread-safety</span><span class="sxs-lookup"><span data-stu-id="3396e-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="3396e-106">Applicazioni STA e MTA</span><span class="sxs-lookup"><span data-stu-id="3396e-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="3396e-107">Considerazioni sul threading di Windows Form</span><span class="sxs-lookup"><span data-stu-id="3396e-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="3396e-108">Considerazioni sugli Appunti</span><span class="sxs-lookup"><span data-stu-id="3396e-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="3396e-109">Eccezioni nei gestori eventi</span><span class="sxs-lookup"><span data-stu-id="3396e-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="3396e-110">Eliminazione di oggetti e controlli</span><span class="sxs-lookup"><span data-stu-id="3396e-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="3396e-111">API StylusInput</span><span class="sxs-lookup"><span data-stu-id="3396e-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="3396e-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="3396e-112">Thread-Safety</span></span>

<span data-ttu-id="3396e-113">Le classi della libreria gestita della piattaforma Tablet PC non sono in genere thread-safe.</span><span class="sxs-lookup"><span data-stu-id="3396e-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="3396e-114">Le raccolte seguenti sono thread-safe a livello di membro. Tuttavia, queste raccolte non garantiscono che un enumeratore sia protetto se un altro thread opera sulla raccolta contemporaneamente:</span><span class="sxs-lookup"><span data-stu-id="3396e-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="3396e-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3396e-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="3396e-116">[Cursori](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3396e-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="3396e-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3396e-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="3396e-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3396e-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="3396e-119">[Riconoscitori](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3396e-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="3396e-120">[Tablet](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3396e-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="3396e-121">Applicazioni STA e MTA</span><span class="sxs-lookup"><span data-stu-id="3396e-121">STA and MTA Applications</span></span>

<span data-ttu-id="3396e-122">Per impostazione predefinita, le applicazioni gestite create usando le procedure guidate contenute in Microsoft Visual Studio .NET sono Apartment a thread singolo (STA).</span><span class="sxs-lookup"><span data-stu-id="3396e-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="3396e-123">È possibile modificare l'Apartment per l'applicazione impostando il thread STA o l'attributo thread dell'Apartment a thread multipli (MTA) nel punto di ingresso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3396e-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="3396e-124">Se l'applicazione viene eseguita in un MTA, è necessario scrivere codice thread-safe; Tuttavia, in questo modo è possibile migliorare determinati problemi di prestazioni di gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="3396e-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="3396e-125">Per ulteriori informazioni sugli attributi thread STA e thread MTA, vedere classe [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) e classe [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="3396e-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="3396e-126">Considerazioni sul threading di Windows Form</span><span class="sxs-lookup"><span data-stu-id="3396e-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="3396e-127">I controlli [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) estendono Windows Form controlli.</span><span class="sxs-lookup"><span data-stu-id="3396e-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="3396e-128">I controlli Windows Form usano il modello di Apartment a thread singolo (STA) perché Windows Form sono basati su finestre Win32 native che sono intrinsecamente a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="3396e-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="3396e-129">Nel codice gestito, i controlli Ink devono essere creati nello stesso thread del thread principale per il form.</span><span class="sxs-lookup"><span data-stu-id="3396e-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="3396e-130">In un'applicazione STA, si verificano determinati eventi in un thread diverso dal thread dell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3396e-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="3396e-131">Quando si chiama un oggetto Windows Form o un controllo, inclusi i controlli [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) , dall'interno di un gestore eventi di Tablet PC, utilizzare il metodo [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) ereditato dell'oggetto o del controllo.</span><span class="sxs-lookup"><span data-stu-id="3396e-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="3396e-132">Per determinare se è necessario, è possibile usare la proprietà [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , ereditata dalla classe Control.</span><span class="sxs-lookup"><span data-stu-id="3396e-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="3396e-133">Ad esempio, nel gestore eventi seguente per l'evento di [riconoscimento](/previous-versions/ms829424(v=msdn.10)) , la proprietà [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) viene verificata e, se **true**, il gestore eventi viene richiamato dal thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3396e-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="3396e-134">Se si inserisce un [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) in awebpagein in un browser (vedere [controlli Web](web-controls.md)), viene eseguito come applicazione sta.</span><span class="sxs-lookup"><span data-stu-id="3396e-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="3396e-135">Per le applicazioni smart client (vedere [No Touch Deployment](no-touch-deployment.md)), lo sviluppatore ha il controllo completo sulla [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="3396e-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="3396e-136">Il valore predefinito è in genere STA, ma può essere MTA, a seconda della versione di CLR. Per problemi di threading che coinvolgono il metodo [**RealTimeStylus**](realtimestylus-class.md), vedere [considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="3396e-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="3396e-137">Per ulteriori informazioni sulla chiamata di Windows Form da un'applicazione MTA, vedere [esempio di controllo multithreading Windows Form](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="3396e-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="3396e-138">Considerazioni sugli Appunti</span><span class="sxs-lookup"><span data-stu-id="3396e-138">Clipboard Considerations</span></span>

<span data-ttu-id="3396e-139">L'oggetto [Appunti](../dataxchg/clipboard.md) funziona solo da un thread sta.</span><span class="sxs-lookup"><span data-stu-id="3396e-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="3396e-140">Quando si tenta di copiare o incollare dagli Appunti da un thread che non è STA, si ottiene un [ThreadStateException](/previous-versions/windows/).</span><span class="sxs-lookup"><span data-stu-id="3396e-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="3396e-141">Se l'applicazione è MTA, creare un thread STA per gestire le chiamate al metodo degli Appunti e alcuni degli altri aspetti dell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3396e-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="3396e-142">Eccezioni nei gestori eventi</span><span class="sxs-lookup"><span data-stu-id="3396e-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="3396e-143">Le eccezioni non possono essere generate dall'interno dei gestori di eventi di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3396e-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="3396e-144">Se, ad esempio, un delegato del gestore eventi per un oggetto o una raccolta di Tablet PC ha tre gestori registrati e il primo genera un'eccezione, si verifica la sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="3396e-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="3396e-145">Il primo gestore si chiude.</span><span class="sxs-lookup"><span data-stu-id="3396e-145">The first handler exits.</span></span>
2.  <span data-ttu-id="3396e-146">L'eccezione viene persa.</span><span class="sxs-lookup"><span data-stu-id="3396e-146">The exception is lost.</span></span>
3.  <span data-ttu-id="3396e-147">I gestori rimanenti non vengono richiamati.</span><span class="sxs-lookup"><span data-stu-id="3396e-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="3396e-148">Eliminazione di oggetti e controlli</span><span class="sxs-lookup"><span data-stu-id="3396e-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="3396e-149">Per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi oggetto o controllo di Tablet PC a cui è stato collegato un gestore eventi prima che l'oggetto o il controllo esca dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="3396e-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="3396e-150">Per migliorare le prestazioni nell'applicazione, eliminare manualmente qualsiasi oggetto o controllo di Tablet PC che implementi il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) quando l'oggetto o il controllo non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="3396e-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="3396e-151">API StylusInput</span><span class="sxs-lookup"><span data-stu-id="3396e-151">StylusInput APIs</span></span>

<span data-ttu-id="3396e-152">Per informazioni sulle considerazioni relative al threading per l'oggetto [**RealTimeStylus**](realtimestylus-class.md) e le API (Application Programming Interface) di StylusInput, vedere [considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="3396e-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
