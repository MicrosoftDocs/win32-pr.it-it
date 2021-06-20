---
title: Uso dell'elemento Stroke
description: Questo articolo descrive l'uso dell'elemento Stroke di VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web workshop, elemento stroke
- progettazione di pagine Web, elemento stroke
- Vector Markup Language (VML), elemento stroke
- VML (Vector Markup Language),elemento stroke
- grafica vettoriale, elemento stroke
- Elemento stroke
- Elementi VML, tratto
- Forme VML, elemento stroke
- Vector Markup Language (VML), attributo della proprietà dashstyle
- VML (Vector Markup Language),attributo della proprietà dashstyle
- vector graphics,dashstyle - attributo della proprietà
- Attributo della proprietà dashstyle
- Vector Markup Language (VML), attributo della proprietà opacità
- VML (Vector Markup Language),attributo della proprietà opacità
- grafica vettoriale, attributo della proprietà opacità
- Attributo della proprietà opacity
- Vector Markup Language (VML), attributo della proprietà linestyle
- VML (Vector Markup Language),attributo della proprietà linestyle
- Vector Graphics, attributo della proprietà linestyle
- Attributo della proprietà linestyle
- Vector Markup Language (VML), attributo della proprietà joinstyle
- VML (Vector Markup Language),attributo della proprietà joinstyle
- vector graphics,joinstyle - attributo della proprietà
- Attributo della proprietà joinstyle
- Vector Markup Language (VML), attributo della proprietà filltype
- VML (Vector Markup Language),attributo della proprietà filltype
- vector graphics, attributo della proprietà filltype
- Attributo della proprietà filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407844"
---
# <a name="using-the-stroke-element"></a>Uso dell'elemento Stroke

Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Uso di `<stroke>`

Come si è appreso, è possibile usare gli attributi di proprietà **strokecolor** e **strokeweight** di una forma predefinita, ad esempio , , , , , , per specificare il colore e lo spessore del contorno di una `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. In questo argomento verrà illustrato come disegnare una forma con una struttura più avanzata.

È possibile inserire il sotto-elemento all'interno di , o o qualsiasi elemento forma predefinito per descrivere come disegnare il `<stroke>` `<shape>` `<shapetype>` contorno della forma. È quindi possibile usare gli attributi della proprietà, ad esempio [dashstyle,](#dashstyle) [opacity,](#opacity) [linestyle,](#linestyle) [joinstyle,](#joinstyle) [filltype,](#filltype) del sotto-elemento per personalizzare `<stroke>` la struttura.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="dashstyle"></a>Dashstyle

È possibile usare **l'attributo della** proprietà dashstyle del `<stroke>` sotto-elemento per disegnare un contorno con vari stili di tratteggio.

**Esempi:**

Se si specifica `<v:stroke dashstyle="solid" />` all'interno `<line>` dell'elemento , è possibile creare una linea continua, come illustrato nella rappresentazione VML seguente:

![solid.gif (96 byte)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Se si modifica l'attributo della proprietà **dashstyle** in "dot", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione VML seguente:

![dot.gif (144 byte)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Se si modifica l'attributo della proprietà **dashstyle** in "dash", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione VML seguente:

![dash.gif (137 byte)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Se si modifica l'attributo della proprietà **dashstyle** in "dashdot", è possibile creare una linea con uno stile tratteggiato e punteggiato, come illustrato nella rappresentazione VML seguente:

![dashdot.gif (145 byte)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Se si modifica l'attributo della proprietà **dashstyle** in "longdash", è possibile creare una linea con uno stile tratteggiato lungo, come illustrato nella rappresentazione VML seguente:

![longdash.gif (123 byte)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Se si modifica l'attributo della proprietà **dashstyle** in "longdashdot", è possibile creare una linea con uno stile tratteggiato e punteggiato lungo, come illustrato nella rappresentazione VML seguente:

![longdashdot.gif (135 byte)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Se si posiziona all'interno dell'elemento , è possibile creare un rettangolo con un contorno tratteggiato e punteggiato, come illustrato nella `<v:stroke dashstyle="dashdot" />` `<rect>` rappresentazione VML seguente:

![rect.gif (615 byte)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="opacity"></a>opacità

È possibile usare **l'attributo della proprietà opacità** del sotto-elemento per disegnare un `<stroke>` contorno con vari stili di opacità. Il valore **dell'attributo della proprietà di opacità** può essere qualsiasi numero compreso tra 0 e 1. Per impostazione predefinita, è 1, che indica l'opacità completa.

**Esempi:**

La rappresentazione VML seguente crea una riga con opacità completa:

![line1.gif (96 byte)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Se si aggiunge all'interno dell'elemento , è possibile creare una riga con `<v:stroke opacity="0.5" />` opacità del 50%, come illustrato nella `<line>` rappresentazione VML seguente:

![line2.gif (108 byte)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="linestyle"></a>Linestyle

È possibile usare **l'attributo della** proprietà linestyle del `<stroke>` sotto-elemento per disegnare un contorno con vari stili di linea.

**Esempi:**

Se si specifica all'interno dell'elemento , è possibile creare un rettangolo con un singolo `<v:stroke linestyle="single" />` `<rect>` contorno, come illustrato nella rappresentazione VML seguente:

![single.gif (537 byte)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Se si modifica l'attributo della proprietà **linestyle** in "thinthin", è possibile creare un rettangolo con il contorno (1:1:1), come illustrato nella rappresentazione VML seguente:

![thinthin.gif (642 byte)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Se si modifica l'attributo della proprietà **linestyle** in "thinthick", è possibile creare un rettangolo con il contorno (1:1:2), come illustrato nella rappresentazione VML seguente:

![thinthick.gif (646 byte)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Se si modifica l'attributo della proprietà **linestyle** in "thickthin", è possibile creare un rettangolo con il contorno (2:1:1), come illustrato nella rappresentazione VML seguente:

![thickthin.gif (676 byte)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Se si modifica l'attributo della proprietà **linestyle** in "thickbetweenthin", è possibile creare un rettangolo con il contorno (1:1:2:1:1), come illustrato nella rappresentazione VML seguente:

![thickbthin.gif (669 byte)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="joinstyle"></a>joinstyle

È possibile usare **l'attributo joinstyle** del `<stroke>` sotto-elemento per definire la modalità di unione delle linee.

Ad esempio, per creare una forma con la struttura round join, come illustrato nella figura seguente, è possibile specificare all'interno dell'elemento , come illustrato nella rappresentazione `<v:stroke joinstyle="round" />` `<polyline>` VML seguente:

![round.gif (660 byte)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Se si modifica l'attributo della proprietà **joinstyle** in "smussatura", è possibile creare una forma con il contorno smussato, come illustrato nella rappresentazione VML seguente:

![bevel.gif (650 byte)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Se si modifica l'attributo della proprietà **joinstyle** in "miter", è possibile creare una forma con la struttura miter-join, come illustrato nella rappresentazione VML seguente:

![miter.gif (702 byte)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="filltype"></a>filltype

È possibile usare **l'attributo della** proprietà filltype del `<stroke>` sotto-elemento per disegnare un contorno con vari effetti di riempimento.

**Esempi:**

Se si specifica all'interno dell'elemento , è possibile creare un rettangolo arrotondato con il contorno con riempimento a tinta unita, come illustrato nella `<v:stroke filltype="solid" />` `<roundrect>` rappresentazione VML seguente:

![solid.gif (701 byte)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Se si modifica l'attributo della proprietà **filltype** in "pattern", si punta l'attributo della proprietà **src** alla posizione del file di immagine del modello e si imposta l'attributo della proprietà **color2** sul secondo colore del motivo, è possibile creare un rettangolo arrotondato con un contorno di motivo, come illustrato nella rappresentazione VML seguente:

![pattern.gif (1055 byte)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Se si modifica l'attributo della proprietà **filltype** in "tile" e si punta l'attributo della proprietà **src** alla posizione del file di immagine, è possibile creare un rettangolo arrotondato con un contorno affiancato, come illustrato nella rappresentazione VML seguente:

![tile.gif (6617 byte)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Se si modifica l'attributo della proprietà **filltype** in "frame" e si punta l'attributo della proprietà **src** alla posizione del file di immagine, è possibile creare un rettangolo arrotondato con un contorno immagine, come illustrato nella rappresentazione VML seguente:

![frame.gif (6203 byte)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 