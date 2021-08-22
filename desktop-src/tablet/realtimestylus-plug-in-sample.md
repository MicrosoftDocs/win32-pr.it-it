---
description: Questa applicazione illustra l'uso della classe RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Esempio di plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a05fd9c70c11130011352d8c16d30abee672e4cd56c000c21b7fbfd2704babe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966880"
---
# <a name="realtimestylus-plug-in-sample"></a>Esempio di plug-in RealTimeStylus

Questa applicazione illustra l'uso [**della classe RealTimeStylus.**](realtimestylus-class.md) Per una panoramica dettagliata delle API StylusInput, inclusa la **classe RealTimeStylus,** vedere Accesso e modifica [dell'input dello stilo](accessing-and-manipulating-stylus-input.md). Per informazioni sui plug-in sincroni e asincroni, vedere [Plug-in e la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Panoramica dell'esempio

Plug-in, gli oggetti che implementano [**l'interfaccia IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) possono essere aggiunti a un [**oggetto RealTimeStylus.**](realtimestylus-class.md) Questa applicazione di esempio usa diversi tipi di plug-in:

-   Plug-in filtro pacchetti: modifica i pacchetti. Il plug-in filtro pacchetti in questo esempio modifica le informazioni sui pacchetti vincolando tutti i dati dei pacchetti (x,y) all'interno di un'area rettangolare.
-   Plug-in renderer dinamico personalizzato: modifica le qualità di rendering dinamico. Il plug-in per il rendering dinamico personalizzato in questo esempio modifica il modo in cui viene eseguito il rendering dell'input penna disegnando un piccolo cerchio intorno a ogni punto (x,y) di un tratto.
-   Plug-in renderer dinamico: modifica le qualità di rendering dinamico. Questo esempio illustra l'uso [**dell'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) come plug-in per gestire il rendering dinamico dell'input penna.
-   Plug-in riconoscimento movimenti: riconosce i movimenti dell'applicazione. Questo esempio illustra l'uso dell'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) come plug-in per riconoscere i movimenti dell'applicazione (quando è in esecuzione in un sistema con il riconoscimento movimenti Microsoft presente).

Questo esempio fornisce inoltre un'interfaccia utente che consente all'utente di aggiungere, rimuovere e modificare l'ordine di ogni plug-in nella raccolta. La soluzione di esempio contiene due progetti, RealTimeStylusPluginApp e RealTimeStylusPlugins. RealTimeStylusPluginApp contiene l'interfaccia utente per l'esempio. RealTimeStylusPlugins contiene le implementazioni dei plug-in. Il progetto RealTimeStylusPlugins definisce lo spazio dei nomi RealTimeStylusPlugins, che contiene il filtro di pacchetti e i plug-in del renderer dinamici personalizzati. Questo spazio dei nomi fa riferimento al progetto RealTimeStylusPluginApp. Il progetto RealTimeStylusPlugins usa gli spazi dei nomi [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10))e [Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10))

Per una panoramica degli spazi dei nomi [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) e [Microsoft.StylusInput.PluginData,](/previous-versions/ms823992(v=msdn.10)) vedere Architettura delle [API StylusInput](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Plug-in filtro pacchetti

Il plug-in filtro pacchetti è un plug-in sincrono che illustra la modifica dei pacchetti. In particolare, definisce un rettangolo nel form. Il rendering di tutti i pacchetti disegnati all'esterno dell'area viene eseguito all'interno dell'area. La classe plug-in `PacketFilterPlugin` , , registra per la notifica degli eventi di input , e della `StylusDown` `StylusUp` `Packets` penna. La classe implementa i [metodi StylusDown,](/previous-versions/ms824761(v=msdn.10)) [StylusUp](/previous-versions/ms824764(v=msdn.10)) [e Packets](/previous-versions/ms824756(v=msdn.10)) definiti nella [**classe IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)

Il costruttore pubblico per `PacketFilterPlugin` richiede una [struttura Rectangle.](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) Questo rettangolo definisce l'area rettangolare, in coordinate dello spazio input penna (.01mm = 1 unità HIMETRIC), in cui verranno contenuti i pacchetti. Il rettangolo viene mantenuto in un campo privato, `rectangle` .


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



La classe registra per le notifiche degli eventi implementando la `PacketFilterPlugin` funzione di accesso get per la proprietà [DataInterest.](/previous-versions/ms824752(v=msdn.10)) In questo caso, il plug-in è interessato a rispondere alle notifiche `StylusDown` `Packets` , , e `StylusUp` `Error` . L'esempio restituisce questi valori come definito [nell'enumerazione DataInterestMask.](/previous-versions/ms824787(v=msdn.10)) Il [metodo StylusDown](/previous-versions/ms824761(v=msdn.10)) viene chiamato quando la punta della penna contatta la superficie del digitalizzatore. Il [metodo StylusUp](/previous-versions/ms824764(v=msdn.10)) viene chiamato quando la punta della penna esce dalla superficie del digitalizzatore. Il [metodo Packets](/previous-versions/ms824756(v=msdn.10)) viene chiamato quando [**l'oggetto RealTimeStylus**](realtimestylus-class.md) riceve pacchetti. Il [metodo Error](/previous-versions/ms585069(v=vs.100)) viene chiamato quando il plug-in corrente o un plug-in precedente genera un'eccezione.


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



La `PacketFilterPlugin` classe gestisce la maggior parte di queste notifiche in un metodo helper, `ModifyPacketData` . Il `ModifyPacketData` metodo ottiene i valori x e y per ogni nuovo pacchetto dalla classe [PacketsData.](/previous-versions/ms824590(v=msdn.10)) Se uno dei due valori si trova all'esterno del rettangolo, il metodo sostituisce il valore con il punto più vicino che rientra ancora nel rettangolo. Questo è un esempio di come un plug-in può sostituire i dati del pacchetto quando vengono ricevuti dal flusso di input penna.


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



## <a name="custom-dynamic-renderer-plug-in"></a>Plug-in renderer dinamico personalizzato

La `CustomDynamicRenderer` classe implementa anche la classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) per ricevere notifiche di input penna. Gestisce quindi la notifica `Packets` per disegnare un piccolo cerchio intorno a ogni nuovo punto di pacchetto.

La classe contiene una [variabile Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) che contiene un riferimento all'oggetto grafico passato al costruttore della classe. Si tratta dell'oggetto grafico usato per il rendering dinamico.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Quando il plug-in del renderer dinamico personalizzato riceve una notifica Packets, estrae i dati (x,y) e disegna un piccolo cerchio verde intorno al punto. Questo è un esempio di rendering personalizzato basato sul flusso di input penna.


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



## <a name="the-realtimestyluspluginapp-project"></a>Oggetto RealTimeStylusPluginApp Project

Il progetto RealTimeStylusPluginApp illustra i plug-in descritti in precedenza, nonché i plug-in [**GestureRecognizer**](gesturerecognizer-class.md) e [**DynamicRenderer.**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) L'interfaccia utente del progetto è costituita da:

-   Form contenente un controllo [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) utilizzato per definire l'area di immissione input penna.
-   Controllo [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) per elencare e selezionare i plug-in disponibili.
-   Coppia di [oggetti Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) per consentire il riordino dei plug-in.

Il progetto definisce una struttura , , per semplificare la gestione `PlugInListItem` dei plug-in usati nel progetto. La `PlugInListItem` struttura contiene il plug-in e una descrizione.

La `RealTimeStylusPluginApp` classe stessa implementa la classe [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Questa operazione è necessaria in modo che la classe possa ricevere una notifica quando il `RealTimeStylusPluginApp` plug-in [**GestureRecognizer**](gesturerecognizer-class.md) aggiunge i dati dei movimenti alla coda di output. L'applicazione si registra per la notifica [di CustomStylusDataAdded.](/previous-versions/ms824753(v=msdn.10)) Quando i dati dei movimenti vengono ricevuti, inserisce una relativa descrizione sulla `RealTimeStylusPluginApp` barra di stato nella parte inferiore del modulo.


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
> Nell'implementazione [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) è interessante identificare i dati dei movimenti personalizzati nella coda di output in base al GUID (usando il campo [GestureRecognitionDataGuid)](/previous-versions/ms826344(v=msdn.10)) o per tipo (usando il risultato dell'istruzione as). L'esempio usa entrambe le tecniche di identificazione a scopo dimostrativo. È valido anche uno dei due approcci da solo.

 

Nel gestore dell'evento Load del form, l'applicazione crea istanze delle classi e e le `PacketFilter` aggiunge alla casella di `CustomDynamicRenderer` riepilogo. L'applicazione tenta quindi di creare un'istanza della [**classe GestureRecognizer**](gesturerecognizer-class.md) e, in caso di esito positivo, la aggiunge alla casella di riepilogo. Questa operazione ha esito negativo se il riconoscimento movimenti non è presente nel sistema. Successivamente, l'applicazione crea un'istanza [**di un oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e lo aggiunge alla casella di riepilogo. Infine, l'applicazione abilita ognuno dei plug-in e [**l'oggetto RealTimeStylus**](realtimestylus-class.md) stesso.

Un altro aspetto importante da notare nell'esempio è che nei metodi helper l'oggetto [**RealTimeStylus**](realtimestylus-class.md) viene prima disabilitato prima che i plug-in siano aggiunti o rimossi e quindi ri-abilitati al termine dell'aggiunta o della rimozione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Accesso e modifica dell'input dello stilo](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Plug-in e classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[Esempio di raccolta di input penna RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
