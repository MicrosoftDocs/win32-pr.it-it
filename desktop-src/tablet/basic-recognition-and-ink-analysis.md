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
# <a name="basic-recognition-and-ink-analysis"></a>Riconoscimento di base e analisi dell'input penna

Questo argomento introduce le API di analisi dell'input penna.

## <a name="simple-recognition"></a>Riconoscimento semplice

Le funzionalità di base esposte dall'API di analisi dell'input penna sono l'accesso ai risultati del riconoscimento per un dato input penna. Si tratta di un'operazione semplice e semplice, come illustrato nel codice di esempio seguente.


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



I risultati dell'operazione di riconoscimento sono semplicemente un valore stringa che rappresenta il valore riconosciuto dell'input penna manoscritto. L'API di analisi dell'input penna espone molto più funzionalità di riconoscimento rispetto alla sola stringa riconosciuta, ma questa è l'operazione più comune.

## <a name="incremental-recognition"></a>Riconoscimento incrementale

Il processo di riconoscimento richiede tempo per il completamento, bloccando l'accesso all'applicazione bloccando il thread dell'interfaccia utente dell'applicazione. Può quindi risultare costoso e frustrante per l'utente finale attendere in modo sincrono i risultati. Molte applicazioni Tablet PC richiedono il riconoscimento di più di poche righe di input penna e un approccio incrementale al riconoscimento dei tratti in un thread in background è la strategia ottimale. Il vantaggio di un approccio incrementale anziché un'operazione bulk consiste nel fatto che consente il riconoscimento dei tratti in un determinato periodo di tempo, distribuendo il lavoro sul thread in background anziché in modo sincrono nel thread in primo piano. Per supportare l'analisi incrementale, l'oggetto [**InkAnalyzer**](inkanalyzer.md) dispone di un metodo [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , che gestisce la creazione e la gestione di un thread in background per l'applicazione. Il controllo **InkAnalyzer** gestisce automaticamente anche gli elementi che devono essere riconosciuti e ciò che è già stato riconosciuto.

Sono pertanto disponibili due meccanismi per il raggiungimento dei risultati del riconoscimento:

-   Il metodo [**Analyze**](iinkanalyzer-analyze.md) (analisi sincrona), che funziona meglio per:

    -   Quantità ridotta di input penna.
    -   Quando i risultati sono necessari prima di procedere all'operazione successiva nell'applicazione, ad esempio quando si visualizza un'interfaccia utente di correzione.

-   Metodo [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (analisi asincrona), che funziona meglio per:

    -   Qualsiasi quantità di input penna.
    -   Quando viene utilizzato con un timer che pulsa approssimativamente ogni 600 millisecondi.

> [!Note]  
> 600 millisecondi è la raccomandazione corrente, ma questo intervallo è soggetto a modifiche in sospeso ulteriori test.

 

Per utilizzare l'operazione [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , l'oggetto [**InkCollector**](inkcollector-class.md) (o oggetti o controlli simili, ad esempio [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)o [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) gestisce la raccolta e il rendering dei tratti di input penna. Se l'oggetto **InkCollector** è associato alle API di analisi dell'input penna, le applicazioni possono aggiornare i risultati del riconoscimento segnalando a [**InkAnalyzer**](inkanalyzer.md) ogni nuovo tratto aggiunto all'applicazione. Ciò consente all' **oggetto InkAnalyzer** di riconoscere i tratti in modo incrementale e in un thread in background.

Per eseguire l'analisi in background incrementale, le applicazioni devono implementare tre passaggi (visualizzati per il codice gestito):

1. Aggiungere il tratto a [**InkAnalyzer**](inkanalyzer.md) ogni volta che viene generato l'evento [**Stroke**](inkoverlay-stroke.md) dell'oggetto [**InkOverlay**](inkoverlay-class.md) :


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



2. Richiamare le operazioni [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) a un intervallo definito.


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
> Nota le applicazioni non devono semplicemente richiamare l'operazione di analisi in background dopo ogni nuovo tratto. Questa operazione avrà esito negativo (restituendo un valore **false**) se è già in esecuzione un'operazione in background. Il motivo di questo comportamento consiste nel limitare il numero di thread in background e le operazioni di riconciliazione necessarie.

 

3. Ascolto dell'evento [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (codice gestito) o dell'evento [**results**](-ianalysisevents-results.md) (codice C++) per determinare quando il processo in background è terminato:


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



Ora che l'elaborazione dell'input penna viene eseguita in un thread in background, l'applicazione è in grado di accettare le modifiche apportate all'input penna mentre l'operazione in background funziona. Questa operazione non è possibile se si usa un thread sincrono. Il lavoro viene eseguito sul thread dell'interfaccia utente, bloccando la possibilità di apportare modifiche. Le modifiche includono l'aggiunta di più input penna al documento, l'eliminazione di input penna o la trasformazione della posizione o dell'aspetto dell'input penna esistente. Le modifiche che si verificano durante l'operazione in background possono infatti invalidare i risultati. Se ad esempio si elimina un tratto da una parola, viene modificato il valore di riconoscimento della parola. L'API [**InkAnalyzer**](inkanalyzer.md) prevede un processo di riconciliazione incorporato che determina automaticamente le parti dell'operazione in background che risultano non valide in seguito alla modifica dell'input penna durante l'analisi.

Il processo di riconciliazione automatica viene eseguito a causa di tre fattori:

1.  Proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) .

    -   Ogni volta che l'applicazione aggiunge (metodo [**AddStroke**](iinkanalyzer-addstroke.md) ) o rimuove (metodo [**RemoveStroke**](iinkanalyzer-removestroke.md) ) un tratto da o verso l' [**oggetto InkAnalyzer**](inkanalyzer.md), la posizione fisica del tratto viene acquisita e la volta successiva che viene richiamata un'operazione di analisi, l' **oggetto InkAnalyzer** garantisce che il tratto o l'area occupata da tale tratto venga analizzato.
    -   Ogni volta che l'applicazione modifica l'input penna esistente, modifica il percorso o modifica altri attributi di disegno dell'input penna, è possibile aggiungere la posizione della modifica (i limiti dell'input penna) alla proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) di [**InkAnalyzer**](inkanalyzer.md). In questo modo si garantisce che la volta successiva in cui l'applicazione avvierà l'operazione di analisi venga verificata la presenza di risultati corretti.
    -   In questo modo, la proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) tiene traccia, tra le esecuzioni di analisi, delle aree del documento e, a sua volta, che devono essere verificate la correttezza dei risultati di analisi e riconoscimento dell'input penna.

2.  Analisi limitata.

    -   Ogni volta che l'applicazione richiama l'operazione di analisi, la proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica i tratti che devono essere analizzati. In questo modo l'operazione di analisi consente di limitare l'operazione solo alle aree dirty e ignorare tutte le altre aree, ottimizzando la quantità di tempo impiegato per la ripetizione dell'analisi dell'input penna.
    -   [**InkAnalyzer**](inkanalyzer.md) non ignora completamente tutte le altre aree della pagina, ma può esaminare le aree adiacenti per determinare se le modifiche apportate nell'area dirty hanno effetto sulle aree adiacenti. Ad esempio, l'analizzatore classifica "is" nell'esempio di input penna seguente come singolo tipo **InkWord** della classe [**ContextNode**](icontextnode.md) :

!["is" scritto a mano](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

L'eliminazione dei risultati "s" in un'area dirty (contrassegnata con una casella rossa).

!["i" scritto a mano](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Dopo l'analisi, l'analizzatore modifica la classificazione per "I" in un tipo **InkDrawing** , anche se è al di fuori dell'area dirty, perché senza il tratto "s" di supporto l'analizzatore di input penna ha una probabilità 50/50 dell'input penna Classificato come un disegno o una parola.

-   Stato interno memorizzato nella cache.

    -   Quando un'applicazione richiama un'operazione di analisi in background, [**InkAnalyzer**](inkanalyzer.md) memorizza nella cache uno snapshot dei dati eliminati. Se si acquisisce uno snapshot, l' **oggetto InkAnalyzer** può lavorare per analizzare i dati indipendentemente dai dati usati dall'applicazione oppure usare lo snapshot come punto di confronto per determinare quali modifiche sono state apportate dall'applicazione durante l'analisi in background.
    -   La memorizzazione nella cache dello stato e il confronto delle modifiche è preferibile rispetto al mantenimento di un elenco di tutte le modifiche apportate per un motivo principale: proxy di dati. Si tratta di uno scenario avanzato descritto più avanti in questo documento, ma prevede che l'applicazione aggiorni l' [**oggetto InkAnalyzer**](inkanalyzer.md) con solo i dati di input penna e non input penna correnti prima dell'operazione di analisi richiamata e prima di elaborare i risultati di un'operazione di analisi.

## <a name="simple-ink-analysis"></a>Analisi input penna semplice

I due scenari precedenti, ovvero il riconoscimento semplice e il riconoscimento incrementale, descrivono come accedere ai valori di riconoscimento senza menzionare come accedere ai risultati dell'analisi dell'input penna o della classificazione. La configurazione predefinita di [**InkAnalyzer**](inkanalyzer.md)esegue sia algoritmi di analisi dell'input penna che algoritmi di riconoscimento. Questa configurazione produce i risultati più accurati, perché le due tecnologie interagiscono per migliorare l'accuratezza. Ovvero i motori di analisi dell'input penna consentono di separare il disegno dalla scrittura e normalizzare la scrittura angolata in un piano orizzontale, ovvero il piano di input ottimale per i motori di riconoscimento.

Per accedere ai risultati dell'analisi dell'input penna, l'applicazione usa i metodi [**Analyze**](iinkanalyzer-analyze.md) o [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) esattamente come descritto nei due scenari di riconoscimento precedenti. Non viene apportata alcuna modifica perché gli algoritmi di analisi e riconoscimento dell'input penna sono già in esecuzione quando vengono chiamati tali metodi. Tuttavia, l'accesso ai risultati è più complicato rispetto alla lettura del valore di una stringa. Nell'esempio di codice seguente, ad esempio, vengono illustrati il raggruppamento e le posizioni di tutti i segmenti **InkWord** e **InkDrawing** eseguendo il rendering di un rettangolo attorno al gruppo di tratti che costituiscono la classificazione.

Questo esempio usa semplicemente l'evento **Paint** del modulo per eseguire il rendering di rettangoli colorati intorno alle parole o ai disegni. Il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) restituisce una raccolta di oggetti esistente solo se l'operazione di analisi è stata eseguita e i risultati contengono le classificazioni con il tipo [**ContextNode**](icontextnode.md) specificato. Se nel documento non è presente alcun **ContextNode** del tipo desiderato, i passaggi per creare i rettangoli vengono ignorati.

Ogni oggetto restituito dal metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) avrà proprietà correlate a tale tipo di classificazione. L'oggetto **InkWordNode** , ad esempio, fa riferimento a tutti i tratti che costituiscono una singola parola nel documento e fa riferimento alla stringa riconosciuta per la parola. **InkDrawingNode** fa riferimento a tutti i tratti che compongono il singolo disegno nel documento e fanno riferimento al nome della forma per il disegno.

Il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) è molto simile al metodo [**DivisionResult:: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) che ha restituito raccolte di [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) di tipi di scrittura o di disegno.


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



Per inserire l'esempio di codice precedente in prospettiva, prendere in considerazione l'esempio di input penna seguente:

![esempio di input penna "questo è un input penna". con un cerchio sotto di esso](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Se si chiama il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e si passa il campo statico per **InkWord**, l'analizzatore restituisce una raccolta di quattro oggetti **InkWordNode** :

![output dell'analizzatore, "questo è un input penna"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Se si chiama il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e si passa il campo statico per **InkDrawing**, l'analizzatore restituisce una raccolta di un oggetto **InkDrawingNode** :

![immagine che mostra "Oval", il risultato di InkDrawing Analyzer](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Una volta generato l'evento **Paint** , il codice di esempio esegue il rendering dei rettangoli intorno a ogni oggetto:

![disegno originale con rettangoli sottoposti a rendering intorno all'oggetto e alle parole](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

Questo esempio riguarda solo il metodo [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) , ma poiché i motori di analisi dell'input penna sono in grado di rilevare un set più completo di tipi di input penna, il metodo corrisponde anche a tutti i tipi di nodi rilevabili dai motori di analisi dell'input penna, ad esempio linee, paragrafi e altre strutture.

## <a name="using-ink-analysis-with-point-erase"></a>Uso dell'analisi dell'input penna con cancellazione punti

L'applicazione deve apportare modifiche nel modo in cui aggiorna i tratti quando esegue la cancellazione dei punti per garantire prestazioni ottimali. In primo luogo, a livello di applicazione, sostituire il punto dello stilo del tratto esistente con il punto dello stilo del nuovo tratto, quindi chiamare [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) su tale tratto e aggiornare l'area dirty con i limiti del tratto. In questo modo, l' [**oggetto InkAnalyzer**](inkanalyzer.md) recupererà i dati del tratto aggiornati al momento dell'avvio del successivo ciclo di analisi in background. Questa tecnica è illustrata nell'esempio seguente.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'analisi dell'input penna](ink-analysis-overview.md)
</dt> <dt>

[Utilizzo API analisi input penna](ink-analysis-api-usage.md)
</dt> </dl>

 

 
