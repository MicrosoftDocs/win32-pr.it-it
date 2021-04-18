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
# <a name="realtimestylus-ink-collection-sample"></a>Esempio di raccolta inchiostro RealTimeStylus

Questa applicazione illustra il rendering e la raccolta di input penna quando si usa la classe [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="the-inkcollection-project"></a>Progetto InkCollection

Questo esempio è costituito da una singola soluzione che contiene un progetto, InkCollection. L'applicazione definisce lo `InkCollection` spazio dei nomi che contiene una singola classe, denominata anche `InkCollection` . La classe eredita dalla classe del [form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa l'interfaccia [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



La classe InkCollection definisce un set di costanti private utilizzate per specificare diversi spessori di input penna. La classe dichiara anche istanze private della classe [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , la classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` e la classe [renderer](/previous-versions/ms828481(v=msdn.10)) `myRenderer` . **DynamicRenderer** esegue il rendering del [tratto](/previous-versions/ms552692(v=vs.100)) attualmente in fase di raccolta. L'oggetto Renderer, `myRenderer` , esegue il rendering degli oggetti Stroke che sono già stati raccolti.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



La classe dichiara anche un oggetto [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , usato per archiviare i dati dei pacchetti raccolti da uno o più oggetti [Cursor](/previous-versions/ms552104(v=vs.100)) . I valori [ID](/previous-versions/ms824826(v=msdn.10)) dell'oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) vengono utilizzati come chiave Hashtable per identificare in modo univoco i dati dei pacchetti raccolti per un determinato oggetto cursore.

Un'istanza privata dell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) , `myInk` , archivia gli oggetti [Stroke](/previous-versions/ms552692(v=vs.100)) raccolti da `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>Evento di caricamento del form

Nel gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) per il form, `myDynamicRenderer` viene creata un'istanza di tramite l'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) che accetta un controllo come argomento e `myRenderer` viene costruito con un costruttore senza argomenti.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Prestare attenzione al commento che segue la creazione di un'istanza dei renderer, perché `myDynamicRenderer` utilizza i valori predefiniti per [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) durante il rendering dell'input penna. Si tratta di un comportamento standard. Tuttavia, se si desidera assegnare al rendering dell'input penna `myDynamicRenderer` un aspetto diverso da quello di input penna eseguito da `myRenderer` , è possibile modificare la proprietà [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) in `myDynamicRenderer` . A tale scopo, rimuovere il commento dalle righe seguenti prima di compilare ed eseguire l'applicazione.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



Successivamente, l'applicazione crea l'oggetto [**RealTimeStylus**](realtimestylus-class.md) usato per ricevere le notifiche dello stilo e aggiunge l'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) alla coda di notifiche del plug-in sincrono. In particolare, `myRealTimeStylus` aggiunge `myDynamicRenderer` alla proprietà [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



Il modulo viene quindi aggiunto alla coda di notifiche del plug-in asincrono. In particolare, `InkCollection` viene aggiunto alla proprietà [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) . Infine, `myRealTimeStylus` e `myDynamicRenderer` sono abilitati e vengono create istanze di pacchetti e myInk.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Oltre ad associare i gestori dei menu per modificare il colore e le dimensioni dell'input penna, prima di implementare l'interfaccia è necessario un blocco di codice più breve. L'esempio deve gestire l'evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del modulo. Nel gestore eventi, l'applicazione deve essere aggiornata `myDynamicRenderer` perché è possibile che un oggetto [Stroke](/previous-versions/ms552692(v=vs.100)) venga raccolto nel momento in cui si verifica l'evento Paint. In tal caso, è necessario ridisegnare la porzione dell'oggetto Stroke che è già stato raccolto. Il [renderer](/previous-versions/ms828481(v=msdn.10)) statico viene usato per ridisegnare gli oggetti Stroke che sono già stati raccolti. Questi tratti si trovano nell'oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) perché vengono inseriti quando vengono disegnati, come illustrato nella sezione successiva.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Implementazione dell'interfaccia IStylusAsyncPlugin

L'applicazione di esempio definisce i tipi di notifiche che è interessato a ricevere nell'implementazione della proprietà [DataInterest](/previous-versions/ms824769(v=msdn.10)) . La proprietà DataInterest definisce quindi le notifiche che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) trasmette al form. Per questo esempio, la proprietà DataInterest definisce l'interesse per le notifiche **StylusDown**, **packets**, **StylusUp** e **Error** tramite l'enumerazione [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .


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



La notifica [StylusDown](/previous-versions/ms824779(v=msdn.10)) si verifica quando la penna tocca la superficie del digitalizzatore. In questo caso, l'esempio alloca una matrice usata per archiviare i dati dei pacchetti per l'oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) . Il [StylusDownData](/previous-versions/ms824107(v=msdn.10)) dal metodo StylusDown viene aggiunto alla matrice e la matrice viene inserita nella tabella hash usando la proprietà [ID](/previous-versions/ms824826(v=msdn.10)) dell'oggetto stilo come chiave.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



La notifica dei [pacchetti](/previous-versions/ms824773(v=msdn.10)) si verifica quando la penna si sposta sulla superficie del digitalizzatore. Quando si verifica questa situazione, l'applicazione aggiunge nuovi [StylusDownData](/previous-versions/ms824107(v=msdn.10)) nella matrice di pacchetti per l'oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) . Questa operazione viene eseguita usando la proprietà [ID](/previous-versions/ms824826(v=msdn.10)) dell'oggetto stilo come chiave per recuperare la matrice di pacchetti per lo stilo dalla tabella hash. I nuovi dati del pacchetto vengono quindi inseriti nella matrice recuperata.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



La notifica [StylusUp](/previous-versions/ms824782(v=msdn.10)) si verifica quando la penna lascia la superficie del digitalizzatore. Quando si verifica questa notifica, nell'esempio viene recuperata la matrice di pacchetti per questo oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) dalla tabella hash che viene rimossa dalla tabella hash perché non è più necessaria, viene aggiunto nei nuovi dati del pacchetto e viene utilizzata la matrice di dati del pacchetto per creare un nuovo oggetto [Stroke](/previous-versions/ms552692(v=vs.100)) `stroke` .


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



Per un esempio in cui viene illustrato un uso più affidabile della classe [**RealTimeStylus**](realtimestylus-class.md) , incluso l'uso della creazione di plug-in personalizzati, vedere [esempio di plug-in RealTimeStylus](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Accesso e modifica dell'input dello stilo](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
