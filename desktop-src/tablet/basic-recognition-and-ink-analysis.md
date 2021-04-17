---
description: Questo argomento introduce le API di analisi dell'input penna.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Riconoscimento di base e analisi dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401519"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="8a461-103">Riconoscimento di base e analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="8a461-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="8a461-104">Questo argomento introduce le API di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="8a461-105">Riconoscimento semplice</span><span class="sxs-lookup"><span data-stu-id="8a461-105">Simple Recognition</span></span>

<span data-ttu-id="8a461-106">Le funzionalità di base esposte dall'API di analisi dell'input penna sono l'accesso ai risultati del riconoscimento per un dato input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="8a461-107">Si tratta di un'operazione semplice e semplice, come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="8a461-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="8a461-108">I risultati dell'operazione di riconoscimento sono semplicemente un valore stringa che rappresenta il valore riconosciuto dell'input penna manoscritto.</span><span class="sxs-lookup"><span data-stu-id="8a461-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="8a461-109">L'API di analisi dell'input penna espone molto più funzionalità di riconoscimento rispetto alla sola stringa riconosciuta, ma questa è l'operazione più comune.</span><span class="sxs-lookup"><span data-stu-id="8a461-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="8a461-110">Riconoscimento incrementale</span><span class="sxs-lookup"><span data-stu-id="8a461-110">Incremental Recognition</span></span>

<span data-ttu-id="8a461-111">Il processo di riconoscimento richiede tempo per il completamento, bloccando l'accesso all'applicazione bloccando il thread dell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a461-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="8a461-112">Può quindi risultare costoso e frustrante per l'utente finale attendere in modo sincrono i risultati.</span><span class="sxs-lookup"><span data-stu-id="8a461-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="8a461-113">Molte applicazioni Tablet PC richiedono il riconoscimento di più di poche righe di input penna e un approccio incrementale al riconoscimento dei tratti in un thread in background è la strategia ottimale.</span><span class="sxs-lookup"><span data-stu-id="8a461-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="8a461-114">Il vantaggio di un approccio incrementale anziché un'operazione bulk consiste nel fatto che consente il riconoscimento dei tratti in un determinato periodo di tempo, distribuendo il lavoro sul thread in background anziché in modo sincrono nel thread in primo piano.</span><span class="sxs-lookup"><span data-stu-id="8a461-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="8a461-115">Per supportare l'analisi incrementale, l'oggetto [**InkAnalyzer**](inkanalyzer.md) dispone di un metodo [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , che gestisce la creazione e la gestione di un thread in background per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a461-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="8a461-116">Il controllo **InkAnalyzer** gestisce automaticamente anche gli elementi che devono essere riconosciuti e ciò che è già stato riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="8a461-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="8a461-117">Sono pertanto disponibili due meccanismi per il raggiungimento dei risultati del riconoscimento:</span><span class="sxs-lookup"><span data-stu-id="8a461-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="8a461-118">Il metodo [**Analyze**](iinkanalyzer-analyze.md) (analisi sincrona), che funziona meglio per:</span><span class="sxs-lookup"><span data-stu-id="8a461-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="8a461-119">Quantità ridotta di input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="8a461-120">Quando i risultati sono necessari prima di procedere all'operazione successiva nell'applicazione, ad esempio quando si visualizza un'interfaccia utente di correzione.</span><span class="sxs-lookup"><span data-stu-id="8a461-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="8a461-121">Metodo [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (analisi asincrona), che funziona meglio per:</span><span class="sxs-lookup"><span data-stu-id="8a461-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="8a461-122">Qualsiasi quantità di input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="8a461-123">Quando viene utilizzato con un timer che pulsa approssimativamente ogni 600 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="8a461-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="8a461-124">600 millisecondi è la raccomandazione corrente, ma questo intervallo è soggetto a modifiche in sospeso ulteriori test.</span><span class="sxs-lookup"><span data-stu-id="8a461-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="8a461-125">Per utilizzare l'operazione [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , l'oggetto [**InkCollector**](inkcollector-class.md) (o oggetti o controlli simili, ad esempio [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)o [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) gestisce la raccolta e il rendering dei tratti di input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="8a461-126">Se l'oggetto **InkCollector** è associato alle API di analisi dell'input penna, le applicazioni possono aggiornare i risultati del riconoscimento segnalando a [**InkAnalyzer**](inkanalyzer.md) ogni nuovo tratto aggiunto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8a461-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="8a461-127">Ciò consente all' **oggetto InkAnalyzer** di riconoscere i tratti in modo incrementale e in un thread in background.</span><span class="sxs-lookup"><span data-stu-id="8a461-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="8a461-128">Per eseguire l'analisi in background incrementale, le applicazioni devono implementare tre passaggi (visualizzati per il codice gestito):</span><span class="sxs-lookup"><span data-stu-id="8a461-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="8a461-129">Aggiungere il tratto a [**InkAnalyzer**](inkanalyzer.md) ogni volta che viene generato l'evento [**Stroke**](inkoverlay-stroke.md) dell'oggetto [**InkOverlay**](inkoverlay-class.md) :</span><span class="sxs-lookup"><span data-stu-id="8a461-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="8a461-130">Richiamare le operazioni [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) a un intervallo definito.</span><span class="sxs-lookup"><span data-stu-id="8a461-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="8a461-131">Nota le applicazioni non devono semplicemente richiamare l'operazione di analisi in background dopo ogni nuovo tratto.</span><span class="sxs-lookup"><span data-stu-id="8a461-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="8a461-132">Questa operazione avrà esito negativo (restituendo un valore **false**) se è già in esecuzione un'operazione in background.</span><span class="sxs-lookup"><span data-stu-id="8a461-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="8a461-133">Il motivo di questo comportamento consiste nel limitare il numero di thread in background e le operazioni di riconciliazione necessarie.</span><span class="sxs-lookup"><span data-stu-id="8a461-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="8a461-134">Ascolto dell'evento [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (codice gestito) o dell'evento [**results**](-ianalysisevents-results.md) (codice C++) per determinare quando il processo in background è terminato:</span><span class="sxs-lookup"><span data-stu-id="8a461-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="8a461-135">Ora che l'elaborazione dell'input penna viene eseguita in un thread in background, l'applicazione è in grado di accettare le modifiche apportate all'input penna mentre l'operazione in background funziona.</span><span class="sxs-lookup"><span data-stu-id="8a461-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="8a461-136">Questa operazione non è possibile se si usa un thread sincrono.</span><span class="sxs-lookup"><span data-stu-id="8a461-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="8a461-137">Il lavoro viene eseguito sul thread dell'interfaccia utente, bloccando la possibilità di apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="8a461-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="8a461-138">Le modifiche includono l'aggiunta di più input penna al documento, l'eliminazione di input penna o la trasformazione della posizione o dell'aspetto dell'input penna esistente.</span><span class="sxs-lookup"><span data-stu-id="8a461-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="8a461-139">Le modifiche che si verificano durante l'operazione in background possono infatti invalidare i risultati.</span><span class="sxs-lookup"><span data-stu-id="8a461-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="8a461-140">Se ad esempio si elimina un tratto da una parola, viene modificato il valore di riconoscimento della parola.</span><span class="sxs-lookup"><span data-stu-id="8a461-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="8a461-141">L'API [**InkAnalyzer**](inkanalyzer.md) prevede un processo di riconciliazione incorporato che determina automaticamente le parti dell'operazione in background che risultano non valide in seguito alla modifica dell'input penna durante l'analisi.</span><span class="sxs-lookup"><span data-stu-id="8a461-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="8a461-142">Il processo di riconciliazione automatica viene eseguito a causa di tre fattori:</span><span class="sxs-lookup"><span data-stu-id="8a461-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="8a461-143">Proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) .</span><span class="sxs-lookup"><span data-stu-id="8a461-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="8a461-144">Ogni volta che l'applicazione aggiunge (metodo [**AddStroke**](iinkanalyzer-addstroke.md) ) o rimuove (metodo [**RemoveStroke**](iinkanalyzer-removestroke.md) ) un tratto da o verso l' [**oggetto InkAnalyzer**](inkanalyzer.md), la posizione fisica del tratto viene acquisita e la volta successiva che viene richiamata un'operazione di analisi, l' **oggetto InkAnalyzer** garantisce che il tratto o l'area occupata da tale tratto venga analizzato.</span><span class="sxs-lookup"><span data-stu-id="8a461-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="8a461-145">Ogni volta che l'applicazione modifica l'input penna esistente, modifica il percorso o modifica altri attributi di disegno dell'input penna, è possibile aggiungere la posizione della modifica (i limiti dell'input penna) alla proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) di [**InkAnalyzer**](inkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="8a461-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="8a461-146">In questo modo si garantisce che la volta successiva in cui l'applicazione avvierà l'operazione di analisi venga verificata la presenza di risultati corretti.</span><span class="sxs-lookup"><span data-stu-id="8a461-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="8a461-147">In questo modo, la proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) tiene traccia, tra le esecuzioni di analisi, delle aree del documento e, a sua volta, che devono essere verificate la correttezza dei risultati di analisi e riconoscimento dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="8a461-148">Analisi limitata.</span><span class="sxs-lookup"><span data-stu-id="8a461-148">Limited analysis.</span></span>

    -   <span data-ttu-id="8a461-149">Ogni volta che l'applicazione richiama l'operazione di analisi, la proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica i tratti che devono essere analizzati.</span><span class="sxs-lookup"><span data-stu-id="8a461-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="8a461-150">In questo modo l'operazione di analisi consente di limitare l'operazione solo alle aree dirty e ignorare tutte le altre aree, ottimizzando la quantità di tempo impiegato per la ripetizione dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="8a461-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="8a461-151">[**InkAnalyzer**](inkanalyzer.md) non ignora completamente tutte le altre aree della pagina, ma può esaminare le aree adiacenti per determinare se le modifiche apportate nell'area dirty hanno effetto sulle aree adiacenti.</span><span class="sxs-lookup"><span data-stu-id="8a461-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="8a461-152">Ad esempio, l'analizzatore classifica "is" nell'esempio di input penna seguente come singolo tipo **InkWord** della classe [**ContextNode**](icontextnode.md) :</span><span class="sxs-lookup"><span data-stu-id="8a461-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

!["is" scritto a mano](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="8a461-154">L'eliminazione dei risultati "s" in un'area dirty (contrassegnata con una casella rossa).</span><span class="sxs-lookup"><span data-stu-id="8a461-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

!["i" scritto a mano](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="8a461-156">Dopo l'analisi, l'analizzatore modifica la classificazione per "I" in un tipo **InkDrawing** , anche se è al di fuori dell'area dirty, perché senza il tratto "s" di supporto l'analizzatore di input penna ha una probabilità 50/50 dell'input penna Classificato come un disegno o una parola.</span><span class="sxs-lookup"><span data-stu-id="8a461-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="8a461-157">Stato interno memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="8a461-157">Internally cached state.</span></span>

    -   <span data-ttu-id="8a461-158">Quando un'applicazione richiama un'operazione di analisi in background, [**InkAnalyzer**](inkanalyzer.md) memorizza nella cache uno snapshot dei dati eliminati.</span><span class="sxs-lookup"><span data-stu-id="8a461-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="8a461-159">Se si acquisisce uno snapshot, l' **oggetto InkAnalyzer** può lavorare per analizzare i dati indipendentemente dai dati usati dall'applicazione oppure usare lo snapshot come punto di confronto per determinare quali modifiche sono state apportate dall'applicazione durante l'analisi in background.</span><span class="sxs-lookup"><span data-stu-id="8a461-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="8a461-160">La memorizzazione nella cache dello stato e il confronto delle modifiche è preferibile rispetto al mantenimento di un elenco di tutte le modifiche apportate per un motivo principale: proxy di dati.</span><span class="sxs-lookup"><span data-stu-id="8a461-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="8a461-161">Si tratta di uno scenario avanzato descritto più avanti in questo documento, ma prevede che l'applicazione aggiorni l' [**oggetto InkAnalyzer**](inkanalyzer.md) con solo i dati di input penna e non input penna correnti prima dell'operazione di analisi richiamata e prima di elaborare i risultati di un'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="8a461-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="8a461-162">Analisi input penna semplice</span><span class="sxs-lookup"><span data-stu-id="8a461-162">Simple Ink Analysis</span></span>

<span data-ttu-id="8a461-163">I due scenari precedenti, ovvero il riconoscimento semplice e il riconoscimento incrementale, descrivono come accedere ai valori di riconoscimento senza menzionare come accedere ai risultati dell'analisi dell'input penna o della classificazione.</span><span class="sxs-lookup"><span data-stu-id="8a461-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="8a461-164">La configurazione predefinita di [**InkAnalyzer**](inkanalyzer.md)esegue sia algoritmi di analisi dell'input penna che algoritmi di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8a461-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="8a461-165">Questa configurazione produce i risultati più accurati, perché le due tecnologie interagiscono per migliorare l'accuratezza.</span><span class="sxs-lookup"><span data-stu-id="8a461-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="8a461-166">Ovvero i motori di analisi dell'input penna consentono di separare il disegno dalla scrittura e normalizzare la scrittura angolata in un piano orizzontale, ovvero il piano di input ottimale per i motori di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8a461-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="8a461-167">Per accedere ai risultati dell'analisi dell'input penna, l'applicazione usa i metodi [**Analyze**](iinkanalyzer-analyze.md) o [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) esattamente come descritto nei due scenari di riconoscimento precedenti.</span><span class="sxs-lookup"><span data-stu-id="8a461-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="8a461-168">Non viene apportata alcuna modifica perché gli algoritmi di analisi e riconoscimento dell'input penna sono già in esecuzione quando vengono chiamati tali metodi.</span><span class="sxs-lookup"><span data-stu-id="8a461-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="8a461-169">Tuttavia, l'accesso ai risultati è più complicato rispetto alla lettura del valore di una stringa.</span><span class="sxs-lookup"><span data-stu-id="8a461-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="8a461-170">Nell'esempio di codice seguente, ad esempio, vengono illustrati il raggruppamento e le posizioni di tutti i segmenti **InkWord** e **InkDrawing** eseguendo il rendering di un rettangolo attorno al gruppo di tratti che costituiscono la classificazione.</span><span class="sxs-lookup"><span data-stu-id="8a461-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="8a461-171">Questo esempio usa semplicemente l'evento **Paint** del modulo per eseguire il rendering di rettangoli colorati intorno alle parole o ai disegni.</span><span class="sxs-lookup"><span data-stu-id="8a461-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="8a461-172">Il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) restituisce una raccolta di oggetti esistente solo se l'operazione di analisi è stata eseguita e i risultati contengono le classificazioni con il tipo [**ContextNode**](icontextnode.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="8a461-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="8a461-173">Se nel documento non è presente alcun **ContextNode** del tipo desiderato, i passaggi per creare i rettangoli vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="8a461-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="8a461-174">Ogni oggetto restituito dal metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) avrà proprietà correlate a tale tipo di classificazione.</span><span class="sxs-lookup"><span data-stu-id="8a461-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="8a461-175">L'oggetto **InkWordNode** , ad esempio, fa riferimento a tutti i tratti che costituiscono una singola parola nel documento e fa riferimento alla stringa riconosciuta per la parola.</span><span class="sxs-lookup"><span data-stu-id="8a461-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="8a461-176">**InkDrawingNode** fa riferimento a tutti i tratti che compongono il singolo disegno nel documento e fanno riferimento al nome della forma per il disegno.</span><span class="sxs-lookup"><span data-stu-id="8a461-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="8a461-177">Il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) è molto simile al metodo [**DivisionResult:: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) che ha restituito raccolte di [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) di tipi di scrittura o di disegno.</span><span class="sxs-lookup"><span data-stu-id="8a461-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="8a461-178">Per inserire l'esempio di codice precedente in prospettiva, prendere in considerazione l'esempio di input penna seguente:</span><span class="sxs-lookup"><span data-stu-id="8a461-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![esempio di input penna "questo è un input penna".](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="8a461-181">Se si chiama il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e si passa il campo statico per **InkWord**, l'analizzatore restituisce una raccolta di quattro oggetti **InkWordNode** :</span><span class="sxs-lookup"><span data-stu-id="8a461-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![output dell'analizzatore, "questo è un input penna"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="8a461-183">Se si chiama il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e si passa il campo statico per **InkDrawing**, l'analizzatore restituisce una raccolta di un oggetto **InkDrawingNode** :</span><span class="sxs-lookup"><span data-stu-id="8a461-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![immagine che mostra "Oval", il risultato di InkDrawing Analyzer](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="8a461-185">Una volta generato l'evento **Paint** , il codice di esempio esegue il rendering dei rettangoli intorno a ogni oggetto:</span><span class="sxs-lookup"><span data-stu-id="8a461-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![disegno originale con rettangoli sottoposti a rendering intorno all'oggetto e alle parole](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="8a461-187">Questo esempio riguarda solo il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) , ma poiché i motori di analisi dell'input penna sono in grado di rilevare un set più completo di tipi di input penna, il metodo corrisponde anche a tutti i tipi di nodi rilevabili dai motori di analisi dell'input penna, ad esempio linee, paragrafi e altre strutture.</span><span class="sxs-lookup"><span data-stu-id="8a461-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="8a461-188">Uso dell'analisi dell'input penna con cancellazione punti</span><span class="sxs-lookup"><span data-stu-id="8a461-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="8a461-189">L'applicazione deve apportare modifiche nel modo in cui aggiorna i tratti quando esegue la cancellazione dei punti per garantire prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="8a461-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="8a461-190">In primo luogo, a livello di applicazione, sostituire il punto dello stilo del tratto esistente con il punto dello stilo del nuovo tratto, quindi chiamare [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) su tale tratto e aggiornare l'area dirty con i limiti del tratto.</span><span class="sxs-lookup"><span data-stu-id="8a461-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="8a461-191">In questo modo, l' [**oggetto InkAnalyzer**](inkanalyzer.md) recupererà i dati del tratto aggiornati al momento dell'avvio del successivo ciclo di analisi in background.</span><span class="sxs-lookup"><span data-stu-id="8a461-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="8a461-192">Questa tecnica è illustrata nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="8a461-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="8a461-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a461-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a461-194">Panoramica dell'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="8a461-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="8a461-195">Utilizzo API analisi input penna</span><span class="sxs-lookup"><span data-stu-id="8a461-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
