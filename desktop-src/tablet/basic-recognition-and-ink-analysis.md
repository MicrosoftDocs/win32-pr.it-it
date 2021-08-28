---
description: Questo argomento presenta le API di analisi dell'input penna.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Riconoscimento di base e analisi dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4bdfa0d93c25e397caf0f116f0f47b303e9571d342825673572011534404de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111339"
---
# <a name="basic-recognition-and-ink-analysis"></a>Riconoscimento di base e analisi dell'input penna

Questo argomento presenta le API di analisi dell'input penna.

## <a name="simple-recognition"></a>Riconoscimento semplice

La funzionalità di base esposta dall'API di analisi dell'input penna è l'accesso ai risultati del riconoscimento per una determinata parte di input penna. Questa operazione è semplice e semplice, come illustrato nel codice di esempio seguente.


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



I risultati dell'operazione di riconoscimento sono semplicemente un valore stringa che rappresenta il valore riconosciuto dell'input penna scritto a mano. L'API di analisi dell'input penna espone molte più funzionalità di riconoscimento rispetto alla stringa riconosciuta, ma questa è l'operazione più comune.

## <a name="incremental-recognition"></a>Riconoscimento incrementale

Il completamento del processo di riconoscimento richiede tempo, bloccando l'accesso all'applicazione bloccando il thread dell'interfaccia utente dell'applicazione. Può quindi essere dissabile e frustrante per l'utente finale attendere i risultati in modo sincrono. Molte applicazioni Tablet PC richiedono il riconoscimento di più di poche righe di input penna e un approccio incrementale al riconoscimento dei tratti in un thread in background è la strategia ottimale. Il vantaggio di un approccio incrementale invece di un'operazione in blocco è che consente il riconoscimento dei tratti per un periodo di tempo, stendendo il lavoro sul thread in background anziché in modo sincrono sul thread in primo piano. Per supportare l'analisi incrementale, l'oggetto [**InkAnalyzer**](inkanalyzer.md) dispone di un metodo [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) che gestisce la creazione e la gestione di un thread in background per l'applicazione. **InkAnalyzer** si occupa anche automaticamente di gestire ciò che deve essere riconosciuto e ciò che è già stato riconosciuto.

Esistono quindi due meccanismi per ottenere i risultati del riconoscimento:

-   Il [**metodo Analyze**](iinkanalyzer-analyze.md) (analisi sincrona), che funziona meglio per:

    -   Piccole quantità di input penna.
    -   Quando i risultati sono necessari prima di procedere all'operazione successiva nell'applicazione, ad esempio quando si visualizza un'interfaccia utente di correzione.

-   Il [**metodo BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (analisi asincrona), che funziona meglio per:

    -   Qualsiasi quantità di input penna.
    -   Se utilizzato con un timer che pulsa circa ogni 600 millisecondi.

> [!Note]  
> 600 millisecondi è la raccomandazione corrente, ma questo intervallo è soggetto a modifiche in attesa di ulteriori test.

 

Per usare l'operazione [**BackgroundAnalyze,**](iinkanalyzer-backgroundanalyze.md) l'oggetto [**InkCollector**](inkcollector-class.md) (o oggetti o controlli simili come [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)o [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) gestisce la raccolta e il rendering dei tratti input penna. Se **InkCollector** è associato alle API di analisi dell'input penna, le applicazioni possono mantenere aggiornati i risultati del riconoscimento informando [**InkAnalyzer**](inkanalyzer.md) di ogni nuovo tratto aggiunto all'applicazione. Ciò consente a **InkAnalyzer** di riconoscere i tratti in modo incrementale e su un thread in background.

Per eseguire l'analisi in background incrementale, le applicazioni devono implementare tre passaggi (illustrati per il codice gestito):

1. Aggiungere il tratto a [**InkAnalyzer**](inkanalyzer.md) ogni volta che viene generato l'evento [**Stroke**](inkoverlay-stroke.md) dell'oggetto [**InkOverlay:**](inkoverlay-class.md)


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



2. Richiamare le [**operazioni BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) a un intervallo impostato.


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
> Nota Le applicazioni non devono semplicemente richiamare l'operazione di analisi in background dopo ogni nuovo tratto. Se un'operazione in background è già in esecuzione, l'operazione avrà esito negativo(restituisce il valore **false).** Il motivo di questo comportamento è limitare il numero di thread in background e le operazioni di riconciliazione necessarie.

 

3. Restare in ascolto [dell'evento ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (codice gestito) o [**results**](-ianalysisevents-results.md) (codice C++) per determinare quando il processo in background è stato completato:


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



Ora che l'elaborazione dell'input penna viene eseguita su un thread in background, l'applicazione ha la possibilità di accettare modifiche all'input penna mentre l'operazione in background funziona. Se si usa un thread sincrono, questo non è possibile. Il lavoro viene eseguito nel thread dell'interfaccia utente, bloccando la possibilità di apportare modifiche. Le modifiche includono l'aggiunta di altro input penna al documento, l'eliminazione dell'input penna o la trasformazione della posizione o dell'aspetto dell'input penna esistente. Le modifiche che si verificano durante l'operazione in background possono di fatto invalidare i risultati. Ad esempio, l'eliminazione di un tratto da una parola modifica il valore di riconoscimento di tale parola. [**L'API InkAnalyzer**](inkanalyzer.md) ha un processo di riconciliazione incorporato che determina automaticamente quali parti dell'operazione in background diventano non valide in seguito alla modifica dell'input penna durante l'analisi.

Il processo di riconciliazione automatica viene realizzato a causa di tre fattori:

1.  Proprietà [**DirtyRegion.**](iinkanalyzer-getdirtyregion.md)

    -   Ogni volta che l'applicazione aggiunge (metodo [**AddStroke)**](iinkanalyzer-addstroke.md) o rimuove (metodo [**RemoveStroke)**](iinkanalyzer-removestroke.md) un tratto da o verso [**InkAnalyzer**](inkanalyzer.md), la posizione fisica del tratto viene acquisita e alla successiva chiamata di un'operazione di analisi, **InkAnalyzer** assicura che il tratto o l'area occupata da tale tratto sia analizzata.
    -   Ogni volta che l'applicazione modifica l'input penna esistente, modifica la posizione o modifica altri attributi di disegno dell'input penna, la posizione della modifica (i limiti dell'input penna) può essere aggiunta alla proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) di [**InkAnalyzer**](inkanalyzer.md). In questo modo si garantisce che al successivo avvio dell'applicazione l'operazione di analisi in tali aree siano verificati i risultati corretti.
    -   Di conseguenza, la proprietà [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) tiene traccia, tra le esecuzioni di analisi, delle aree del documento e, a sua volta, dei tratti da controllare per verificare i risultati corretti dell'analisi dell'input penna e del riconoscimento.

2.  Analisi limitata.

    -   Ogni volta che l'applicazione richiama l'operazione di analisi, la [**proprietà DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica i tratti da analizzare. Ciò consente all'operazione di analisi di limitare l'operazione solo alle aree dirty e ignorare tutte le altre aree, ottimizzando la quantità di tempo impiegato per la ri-analisi dell'input penna.
    -   [**InkAnalyzer**](inkanalyzer.md) non ignora completamente tutte le altre aree della pagina, ma può invece esaminare le aree adiacenti per determinare se le modifiche apportate nell'area dirty influiscono sulle aree adiacenti. Ad esempio, l'analizzatore classifica "Is", nell'esempio di input penna seguente, come singolo **tipo InkWord** della [**classe ContextNode:**](icontextnode.md)

![scritto a mano "is"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

L'eliminazione delle "s" comporta un'area dirty (contrassegnata con una casella rossa).

!["i" scritto a mano](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Dopo l'analisi, l'analizzatore modifica la classificazione per "I" in un tipo **InkDrawing,** anche se non si trova all'esterno dell'area dirty, perché senza il tratto "s" di supporto, l'analizzatore input penna ha una probabilità di 50/50 che l'input penna venga classificato come disegno o parola.

-   Stato memorizzato nella cache interna.

    -   Quando un'applicazione richiama un'operazione di analisi in [**background, InkAnalyzer**](inkanalyzer.md) memorizza nella cache uno snapshot dei dati potati. Lo snapshot di **InkAnalyzer** può essere usato per analizzare i dati indipendentemente dai dati usati dall'applicazione oppure usare lo snapshot come punto di confronto per determinare le modifiche apportate dall'applicazione durante l'analisi in background.
    -   Caching lo stato e il confronto delle modifiche è meglio che mantenere un elenco di tutte le modifiche che si sono verificate per un motivo principale: proxy dati. Si tratta di uno scenario avanzato descritto più avanti in questo documento, ma prevede l'aggiornamento di [**InkAnalyzer**](inkanalyzer.md) da parte dell'applicazione con solo i dati di input penna e non input penna correnti prima dell'operazione di analisi richiamata e prima dell'elaborazione dei risultati di un'operazione di analisi.

## <a name="simple-ink-analysis"></a>Analisi dell'input penna semplice

I due scenari precedenti (riconoscimento semplice e riconoscimento incrementale) illustrano come accedere ai valori di riconoscimento senza menzionare come accedere ai risultati dell'analisi o della classificazione dell'input penna. La configurazione predefinita di [**InkAnalyzer**](inkanalyzer.md)esegue sia algoritmi di analisi dell'input penna che algoritmi di riconoscimento. Questa configurazione produce i risultati più accurati, perché le due tecnologie lavorano insieme per aumentare l'accuratezza. Ovvero, i motori di analisi dell'input penna consentono di separare il disegno dalla scrittura e normalizzare la scrittura angolare in un piano orizzontale, che è il piano di input ottimale per i motori di riconoscimento.

Per accedere ai risultati dell'analisi dell'input penna, l'applicazione usa i metodi [**Analyze**](iinkanalyzer-analyze.md) o [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) esattamente come descritto nei due scenari di riconoscimento precedenti. Non cambia nulla perché gli algoritmi di analisi e riconoscimento dell'input penna sono già in esecuzione quando questi metodi vengono chiamati. Tuttavia, l'accesso ai risultati è più complicato rispetto alla lettura del valore di una stringa. Ad esempio, l'esempio di codice seguente illustra il raggruppamento e le posizioni di tutti i segmenti **InkWord** e **InkDrawing** tramite il rendering di un rettangolo intorno al gruppo di tratti che costituiscono la classificazione.

Questo esempio usa semplicemente l'evento Paint **form** per eseguire il rendering di rettangoli colorati intorno alle parole o ai disegni. Il [**metodo FindNodesOfType**](iinkanalyzer-findnodesoftype.md) restituisce una raccolta di oggetti che esiste solo se l'operazione di analisi è stata eseguita e i risultati contengono classificazioni con il [**tipo ContextNode**](icontextnode.md) specificato. Se nel documento non è presente alcun **ContextNode** del tipo desiderato, i passaggi per disegnare i rettangoli vengono ignorati.

Ogni oggetto restituito dal [**metodo FindNodesOfType**](iinkanalyzer-findnodesoftype.md) avrà proprietà correlate a tale tipo di classificazione. Ad **esempio, InkWordNode** fa riferimento a tutti i tratti che costituiscono una singola parola nel documento e fa riferimento alla stringa riconosciuta per tale parola. **InkDrawingNode** fa riferimento a tutti i tratti che costituiscono il singolo disegno nel documento e fa riferimento al nome della forma per tale disegno.

Il [**metodo FindNodesOfType**](iinkanalyzer-findnodesoftype.md) è molto simile al metodo [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) che ha restituito raccolte di [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) di tipi di scrittura o disegno.


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



Per mettere in prospettiva l'esempio di codice precedente, si consideri l'esempio di input penna seguente:

![Esempio di input penna "this is some ink". con un cerchio sotto di esso](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Se si chiama il [**metodo FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e si passa il campo statico **per InkWord**, l'analizzatore restituisce una raccolta di quattro **oggetti InkWordNode:**

![output dell'analizzatore, "this is some ink" (Questo è un input penna)](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Se si chiama il [**metodo FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e si passa il campo statico **per InkDrawing**, l'analizzatore restituisce una raccolta di un **oggetto InkDrawingNode:**

![immagine che mostra "oval", il risultato dell'analizzatore di disegno dell'input penna](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Dopo che **Paint** generato l'evento , il codice di esempio esegue il rendering dei rettangoli intorno a ognuno degli oggetti :

![disegno originale con rettangoli di cui viene eseguito il rendering intorno all'oggetto e alle parole](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

Questo esempio tocca solo il metodo [**FindNodesOfType,**](iinkanalyzer-findnodesoftype.md) ma poiché i motori di analisi dell'input penna sono in grado di rilevare un set più completo di tipi di input penna, il metodo corrisponde anche a tutti i tipi di nodi rilevabili dai motori di analisi dell'input penna, ad esempio righe, paragrafi e altre strutture.

## <a name="using-ink-analysis-with-point-erase"></a>Uso dell'analisi dell'input penna con la cancellazione dei punti

L'applicazione deve apportare modifiche al modo in cui aggiorna i tratti durante l'esecuzione della cancellazione del punto per garantire prestazioni ottimali. In primo luogo, a livello dell'applicazione, sostituire il punto dello stilo del tratto esistente con il punto dello stilo del nuovo tratto, quindi chiamare [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) su tale tratto e aggiornare l'area dirty con i limiti del tratto. In questo modo [**InkAnalyzer recupererà**](inkanalyzer.md) i dati aggiornati del tratto all'avvio del successivo ciclo di analisi in background. Questa tecnica è illustrata nell'esempio seguente.


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

[Utilizzo dell'API analisi input penna](ink-analysis-api-usage.md)
</dt> </dl>

 

 
