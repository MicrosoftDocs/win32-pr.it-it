---
description: Dopo la raccolta dell'input penna, le applicazioni possono gestire, manipolare e/o trasferire i dati in altri supporti.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Dati Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de73291269398ae42a47ee26897c8da9bac8abe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525963"
---
# <a name="ink-data"></a>Dati Ink

Dopo la raccolta dell'input penna, le applicazioni possono gestire, manipolare e/o trasferire i dati in altri supporti. Le azioni di selezione, copia, spostamento, salvataggio, visualizzazione e modifica dell'input penna avvengono nell'oggetto [**Ink**](inkdisp-class.md) e nei relativi membri contenuti, ad esempio gli oggetti [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) e [**Collection.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

> [!Note]  
> Utilizzando Real-Time stilo, le applicazioni possono scegliere di mantenere i dati in un formato proprio (ad esempio, il salvataggio di tratti).

 

## <a name="ink-strokes-and-packets"></a>Input penna, tratti e pacchetti

Un oggetto [**Ink**](inkdisp-class.md) è il tipo di dati fondamentale che gestisce, manipola e archivia l'input raccolto dall'oggetto [**InkCollector**](inkcollector-class.md) . Un oggetto **Ink** contiene uno o più oggetti [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) e metodi e proprietà comuni per gestire e modificare tali tratti. Un tratto viene definito come il set di dati acquisito in una singola sequenza di penna, di spostamento e di penna. I dati del tratto contengono una raccolta di pacchetti. Un pacchetto è il set di dati che il dispositivo Tablet Invia a ogni punto di esempio. Questi dati contengono informazioni quali coordinate, pressione della penna, angolo della penna e qualsiasi altro elemento che l'hardware è in grado di trasmettere. La proprietà [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) dell'oggetto **Stroke** descrive i pacchetti generati da un [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

## <a name="strokes"></a>Tratti

È possibile ottenere uno snapshot dei tratti in un oggetto [**Ink**](inkdisp-class.md) usando la proprietà [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) dell'oggetto **Ink** . La proprietà **Strokes** è una raccolta di riferimenti ai tratti nell'oggetto **Ink** nel momento in cui viene letta la proprietà **Strokes** . Se i tratti vengono successivamente aggiunti o eliminati dall'oggetto **Ink** , una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ottenuta in precedenza non viene aggiornata. Inoltre, la proprietà **Strokes** è un valore e, come qualsiasi valore, esce dall'ambito a meno che non sia assegnato a una variabile.

Per mantenerne la sincronizzazione con un [**oggetto Ink**](inkdisp-class.md) , eseguire il wrapping di [**una proprietà in**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) un gestore eventi per gli eventi [**StrokesAdded**](inkstrokes-strokesadded.md) e [**StrokesRemoved**](inkstrokes-strokesremoved.md) nella raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Il gestore deve ottenere una nuova copia della proprietà **Strokes** quando viene generato uno degli eventi. Prestare attenzione a non aggiungere il gestore eventi a una raccolta **Strokes** che non rientra nell'ambito prima che venga generato l'evento.

Si noti che in questo esempio `theAddedStrokesIDs` viene aggiornata con una nuova copia della proprietà Strokes nel `StrokesAdded_Event` gestore.


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a>Proprietà PacketDescription

La proprietà [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) dell'oggetto [**Ink**](inkdisp-class.md) definisce il set di informazioni in ogni pacchetto che l'applicazione ottiene da un dispositivo Tablet PC. Le informazioni in genere includono coordinate, ma possono includere informazioni molto più dettagliate (a seconda delle funzionalità del digitalizzatore di Tablet PC), ad esempio la pressione della penna o l'angolo della penna. Impostando le descrizioni dei pacchetti nell'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) prima che venga raccolto un input penna (usando la proprietà DesiredPacketDescription), si ha il controllo completo sulle proprietà dei dispositivi Tablet PC che si desidera ricevere.

## <a name="extended-properties"></a>Proprietà estese

Le proprietà estese forniscono un meccanismo per il fissaggio dei dati definiti dall'applicazione a [**input penna**](inkdisp-class.md) e ad altri oggetti. Per ulteriori informazioni sulle proprietà estese, vedere la raccolta [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) .

## <a name="ink-rendering"></a>Rendering input penna

L'oggetto [**renderer**](inkrenderer-class.md) è responsabile del rendering dell' [**input penna**](inkdisp-class.md). Dato un contesto appropriato per la tavoletta, l'oggetto **renderer** può mappare le coordinate dello spazio dell'input penna ai pixel, applicare le trasformazioni di visualizzazione e visualizzare l'input penna su schermate e stampanti. I metodi di [**estrazione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) e [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) sono i metodi principali per il rendering dell'input penna. Per ulteriori informazioni sulla visualizzazione di input penna in una finestra, vedere l'oggetto **renderer** .

## <a name="cusps"></a>Cuspidi

Un tratto inizia in genere quando la penna viene ridotta alla superficie di disegno e termina quando viene generata la penna. All'interno di un tratto, i picchi, gli angoli e le modifiche radicali della direzione sono detti cuspidi. Anche gli endpoint di un tratto sono considerati cuspidi. Ad esempio, la lettera maiuscola "L" ha tre cuspidi, una al centro e una a ciascuna estremità.

Quando viene immesso un tratto, viene normalmente smussato e sottoposto a rendering usando una curva di Bézier (o polilinea). Le curve di Bezier possono trasformare le cuspidi in cicli di piccole dimensioni. Ad esempio, il picco della lettera in corsivo "i" potrebbe essere smussato per essere simile alla "e". Per evitare questo problema, i renderer Microsoft hanno una fase "pre-Bezier" che gestisce le cuspidi in modo diverso.

Le cuspidi possono essere utilizzate anche per suddividere gli oggetti [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in unità cancellabili. Se ad esempio si seleziona il lato verticale di una "L" maiuscola, è possibile che venga indicata la cancellazione del lato. La parte del tratto da cancellare è la parte tra due cuspidi.

 

 
