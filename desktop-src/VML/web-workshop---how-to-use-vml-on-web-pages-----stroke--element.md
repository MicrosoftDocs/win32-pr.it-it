---
title: Utilizzo dell'elemento Stroke
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web Workshop, elemento Stroke
- progettazione di pagine Web, elemento Stroke
- Vector Markup Language (la), elemento Stroke
- LA (Vector Markup Language), elemento Stroke
- grafica vettoriale, elemento Stroke
- Stroke-elemento
- Elementi la, Stroke
- Forme la, elemento Stroke
- Vector Markup Language (la), attributo proprietà DashStyle
- LA (Vector Markup Language), attributo proprietà DashStyle
- grafica vettoriale, attributo proprietà DashStyle
- attributo proprietà DashStyle
- Vector Markup Language (la), attributo della proprietà Opacity
- LA (Vector Markup Language), attributo della proprietà Opacity
- Vector graphics, attributo Property Opacity
- attributo della proprietà Opacity
- Vector Markup Language (la), attributo proprietà LineStyle
- LA (Vector Markup Language), attributo proprietà LineStyle
- grafica vettoriale, attributo proprietà LineStyle
- attributo proprietà LineStyle
- Vector Markup Language (la), attributo proprietà joinstyle
- LA (Vector Markup Language), attributo proprietà joinstyle
- grafica vettoriale, attributo proprietà joinstyle
- attributo proprietà joinstyle
- Vector Markup Language (la), attributo proprietà elemento FillType
- LA (Vector Markup Language), attributo proprietà elemento FillType
- grafica vettoriale, attributo proprietà elemento FillType
- attributo proprietà elemento FillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339102"
---
# <a name="using-the-stroke-element"></a>Utilizzo dell'elemento Stroke

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Uso di `<stroke>`

Come si è appreso, è possibile usare gli attributi di proprietà **StrokeColor** e **StrokeWeight** di una forma predefinita, ad esempio `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --per specificare il colore e il peso del contorno di una forma. In questo argomento verrà illustrato come disegnare una forma con una struttura più avanzata.

`<stroke>` `<shape>` Per descrivere come disegnare il contorno della forma, è possibile inserire il sottoelemento all'interno dell'elemento della forma, o `<shapetype>` o di qualsiasi elemento Shape predefinito. È quindi possibile usare gli attributi delle proprietà, ad esempio [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [elemento FillType](#filltype) , del `<stroke>` sottoelemento per personalizzare il contorno.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="dashstyle"></a>DashStyle

È possibile usare l'attributo della proprietà **DashStyle** del `<stroke>` sottoelemento per disegnare una struttura con diversi stili di tratteggio.

**Esempi:**

Se si specifica `<v:stroke dashstyle="solid" />` all'interno dell' `<line>` elemento, è possibile creare una linea continua, come illustrato nella rappresentazione la seguente:

![solid.gif (96 byte)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Se si imposta l'attributo della proprietà **DashStyle** su "dot", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione la seguente:

![dot.gif (144 byte)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Se si imposta l'attributo della proprietà **DashStyle** su "Dash", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione la seguente:

![dash.gif (137 byte)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Se si imposta l'attributo della proprietà **DashStyle** su "DashDot", è possibile creare una riga con uno stile tratteggiato e tratteggiato, come illustrato nella rappresentazione la seguente:

![dashdot.gif (145 byte)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Se si imposta l'attributo della proprietà **DashStyle** su "longdash", è possibile creare una riga con stile tratteggiato lungo, come illustrato nella rappresentazione la seguente:

![longdash.gif (123 byte)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Se si imposta l'attributo della proprietà **DashStyle** su "longdashdot", è possibile creare una linea con uno stile tratteggiato lungo e tratteggiato, come illustrato nella rappresentazione la seguente:

![longdashdot.gif (135 byte)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Se si posiziona `<v:stroke dashstyle="dashdot" />` all'interno dell' `<rect>` elemento, è possibile creare un rettangolo con un contorno tratteggiato e tratteggiato, come illustrato nella rappresentazione la seguente:

![rect.gif (615 byte)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="opacity"></a>opacità

È possibile usare l'attributo della proprietà **Opacity** del `<stroke>` sottoelemento per disegnare un contorno con diversi stili di opacità. Il valore dell'attributo della proprietà **Opacity** può essere qualsiasi numero compreso tra 0 e 1. Per impostazione predefinita, è 1, che indica l'opacità completa.

**Esempi:**

La rappresentazione la seguente crea una riga con opacità completa:

![line1.gif (96 byte)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Se si aggiunge `<v:stroke opacity="0.5" />` all'interno dell' `<line>` elemento, è possibile creare una riga con opacità del 50%, come illustrato nella seguente rappresentazione la:

![line2.gif (108 byte)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="linestyle"></a>LineStyle

È possibile usare l'attributo della proprietà **LineStyle** del `<stroke>` sottoelemento per disegnare un contorno con vari stili di linea.

**Esempi:**

Se si specifica `<v:stroke linestyle="single" />` all'interno dell' `<rect>` elemento, è possibile creare un rettangolo con un unico contorno, come illustrato nella rappresentazione la seguente:

![single.gif (537 byte)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Se si imposta l'attributo della proprietà **LineStyle** su "thinthin", è possibile creare un rettangolo con il contorno (1:1:1), come illustrato nella rappresentazione la seguente:

![thinthin.gif (642 byte)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Se si imposta l'attributo della proprietà **LineStyle** su "thinthick", è possibile creare un rettangolo con il contorno (1:1:2), come illustrato nella rappresentazione la seguente:

![thinthick.gif (646 byte)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Se si imposta l'attributo della proprietà **LineStyle** su "thickthin", è possibile creare un rettangolo con il contorno (2:1:1), come illustrato nella rappresentazione la seguente:

![thickthin.gif (676 byte)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Se si imposta l'attributo della proprietà **LineStyle** su "thickbetweenthin", è possibile creare un rettangolo con il contorno (1:1:2:1:1), come illustrato nella rappresentazione la seguente:

![thickbthin.gif (669 byte)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="joinstyle"></a>joinstyle

È possibile usare l'attributo **joinstyle** del `<stroke>` sottoelemento per definire la modalità di Unione delle linee.

Ad esempio, per creare una forma con il contorno di un round join, come illustrato nella figura seguente, è possibile specificare `<v:stroke joinstyle="round" />` all'interno dell' `<polyline>` elemento, come illustrato nella rappresentazione la seguente:

![round.gif (660 byte)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Se si imposta l'attributo della proprietà **joinstyle** su "smussatura", è possibile creare una forma con il contorno di join smussato, come illustrato nella rappresentazione la seguente:

![bevel.gif (650 byte)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Se si imposta l'attributo della proprietà **joinstyle** su "Miter", è possibile creare una forma con la struttura ad angolo acuto-join, come illustrato nella rappresentazione la seguente:

![miter.gif (702 byte)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="filltype"></a>elemento FillType

È possibile usare l'attributo della proprietà **elemento FillType** del `<stroke>` sottoelemento per disegnare un contorno con vari effetti di riempimento.

**Esempi:**

Se si specifica `<v:stroke filltype="solid" />` all'interno dell' `<roundrect>` elemento, è possibile creare un rettangolo arrotondato con il contorno con riempimento a tinta unita, come illustrato nella rappresentazione la seguente:

![solid.gif (701 byte)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Se si imposta l'attributo della proprietà **elemento FillType** su "pattern", puntare l'attributo della proprietà **src** al percorso del file di immagine del modello e impostare l'attributo della proprietà **color2** sul secondo colore del criterio, è possibile creare un rettangolo arrotondato con un contorno di pattern, come illustrato nella rappresentazione la seguente:

![pattern.gif (1055 byte)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Se si imposta l'attributo della proprietà **elemento FillType** su "Tile" e si posiziona l'attributo della proprietà **src** sul percorso del file di immagine, è possibile creare un rettangolo arrotondato con un contorno affiancato, come illustrato nella rappresentazione la seguente:

![tile.gif (6617 byte)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Se si imposta l'attributo della proprietà **elemento FillType** su "frame" e si posiziona l'attributo della proprietà **src** sul percorso del file di immagine, è possibile creare un rettangolo arrotondato con un contorno immagine, come illustrato nella rappresentazione la seguente:

![frame.gif (6203 byte)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 