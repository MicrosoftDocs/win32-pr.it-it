---
description: Dopo aver raccolto l'input penna, le applicazioni possono gestire, modificare e/o trasferire i dati in altri supporti.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Dati input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f62f566e48859ba2aea7013783b3ccc8c825b8559fdec34e24438d68b6ee65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939411"
---
# <a name="ink-data"></a>Dati input penna

Dopo aver raccolto l'input penna, le applicazioni possono gestire, modificare e/o trasferire i dati in altri supporti. Le azioni di selezione, copia, spostamento, salvataggio, visualizzazione e modifica dell'input penna vengono eseguite sull'oggetto [**Ink**](inkdisp-class.md) e sui relativi membri contenuti, ad esempio la raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e gli oggetti [**Stroke.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

> [!Note]  
> Usando Real-Time Stilo, le applicazioni possono scegliere di mantenere i dati nel proprio formato, ad esempio salvando i tratti.

 

## <a name="ink-strokes-and-packets"></a>Input penna, tratti e pacchetti

Un [**oggetto Ink**](inkdisp-class.md) è il tipo di dati fondamentale che gestisce, modifica e archivia l'input raccolto dall'oggetto [**InkCollector.**](inkcollector-class.md) Un **oggetto Ink** contiene uno o più oggetti [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) e metodi e proprietà comuni per gestire e modificare tali tratti. Un tratto è definito come set di dati acquisiti in una singola sequenza di pen-down, pen-move e pen-up. I dati del tratto contengono una raccolta di pacchetti. Un pacchetto è il set di dati inviati dal dispositivo tablet in ogni punto di campionamento. Questi dati contengono informazioni quali coordinate, pressione della penna, angolo della penna e qualsiasi altro elemento che l'hardware può trasmettere. La [**proprietà PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) dell'oggetto **Stroke** descrive i pacchetti generati da [**un tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)

## <a name="strokes"></a>Tratti

È possibile ottenere uno snapshot dei tratti in un [**oggetto Ink**](inkdisp-class.md) usando la **proprietà** [**Strokes dell'oggetto Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) La **proprietà Strokes** è una raccolta di riferimenti ai tratti nell'oggetto **Ink** al momento della lettura della proprietà **Strokes.** Se i tratti vengono successivamente aggiunti o eliminati **dall'oggetto Ink,** una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ottenuta in precedenza non viene aggiornata. Inoltre, la **proprietà Strokes** è un valore e, come qualsiasi valore, esce dall'ambito a meno che non venga assegnata a una variabile.

Per mantenere [**sincronizzata una**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) proprietà Strokes con un oggetto [**Ink,**](inkdisp-class.md) eseguire il wrapping in un gestore eventi per gli eventi [**StrokesAdded**](inkstrokes-strokesadded.md) e [**StrokesRemoved**](inkstrokes-strokesremoved.md) nella [**raccolta Strokes.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Il gestore deve ottenere una nuova copia della **proprietà Strokes** quando viene generato uno dei due eventi. Prestare attenzione a non aggiungere il gestore eventi a una **raccolta Strokes** che non è in ambito prima che venga generato l'evento.

Si noti che in questo `theAddedStrokesIDs` esempio viene aggiornato con una nuova copia della proprietà strokes nel `StrokesAdded_Event` gestore.


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

La [**proprietà PacketDescription**](inkdisp-class.md) dell'oggetto [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) definisce il set di informazioni in ogni pacchetto che l'applicazione ottiene da un dispositivo Tablet PC. Le informazioni includono in genere le coordinate, ma possono includere informazioni molto più dettagliate (a seconda delle funzionalità del digitalizzatore Tablet PC), ad esempio la pressione della penna o l'angolo della penna. Impostando le descrizioni dei pacchetti nell'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) prima che venga raccolto qualsiasi input penna (usando la proprietà DesiredPacketDescription), si ha il controllo completo su quale delle proprietà dei dispositivi Tablet PC si vuole ricevere.

## <a name="extended-properties"></a>Proprietà estese

Le proprietà estese forniscono un meccanismo per collegare dati definiti dall'applicazione a [**Ink**](inkdisp-class.md) e ad altri oggetti. Per altre informazioni sulle proprietà estese, vedere la [**raccolta ExtendedProperties.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties)

## <a name="ink-rendering"></a>Rendering input penna

[**L'oggetto Renderer**](inkrenderer-class.md) è responsabile del rendering di [**Ink.**](inkdisp-class.md) Dato un contesto di tablet appropriato, l'oggetto **Renderer** può eseguire il mapping delle coordinate dello spazio input penna ai pixel, applicare trasformazioni di visualizzazione e visualizzare l'input penna su schermi e stampanti. I [**metodi Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) e [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) sono i metodi principali per il rendering dell'input penna. Per altre informazioni sulla visualizzazione dell'input penna in una finestra, vedere **l'oggetto Renderer.**

## <a name="cusps"></a>Cuspidi

Un tratto inizia in genere quando la penna viene abbassata sulla superficie di disegno e termina quando la penna viene sollevata. All'interno di un tratto, i picchi, gli angoli e i cambiamenti radicali di direzione sono chiamati cuspe. Anche gli endpoint di un tratto sono considerati cusp. Ad esempio, la lettera maiuscola "L" ha tre caratteri cusp, uno al centro e uno per ogni estremità.

Quando un tratto viene immesso, viene in genere smussato e sottoposto a rendering usando una curva di Bézier (o polilinea). Le curve di Bézier possono trasformare le cuspe in piccoli cicli. Ad esempio, il picco della lettera ricorsiva "i" potrebbe essere smussato in modo da essere simile alla "e" ricorsiva. Per evitare questo problema, i renderer Microsoft hanno una fase di pre-Bézier che gestisce le cusps in modo diverso.

Le cuspe possono essere usate anche per suddividere gli [**oggetti Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in unità cancellabili. Ad esempio, la selezione del lato verticale di una "L" maiuscola potrebbe indicare la cancellazione solo di tale lato. La parte del tratto da cancellare è la parte tra due cusp.

 

 
