---
title: Uso dell'elemento Fill
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web Workshop, elemento Fill
- progettazione di pagine Web, elemento Fill
- Vector Markup Language (la), elemento Fill
- LA (Vector Markup Language), elemento Fill
- grafica vettoriale, elemento Fill
- Fill (elemento)
- Elementi la, Fill
- Forme la, elemento Fill
- Vector Markup Language (la), riempimento sfumato
- LA (Vector Markup Language), riempimento sfumato
- grafica vettoriale, riempimento sfumato
- Forme la, riempimento sfumatura
- forme con riempimento sfumato
- Vector Markup Language (la), riempimento schema
- LA (Vector Markup Language), riempimento modello
- grafica vettoriale, riempimento schema
- Forme la, riempimento schema
- forme con riempimento di modelli
- Vector Markup Language (la), riempimento immagine
- LA (Vector Markup Language), riempimento immagine
- grafica vettoriale, riempimento immagine
- Forme la, riempimento immagine
- forme con riempimento immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104562668"
---
# <a name="using-the-fill-element"></a>Uso dell'elemento Fill

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Come si è appreso, è possibile usare l'attributo della proprietà **FillColor** di un elemento Shape predefinito, ad esempio `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --per specificare il colore usato per riempire la forma. In questo argomento verrà illustrato come disegnare una forma riempita con effetti più avanzati.

È possibile inserire il `<fill>` sottoelemento all'interno dell' `<shape>` elemento della `<shapetype>` forma, o o di qualsiasi elemento della forma predefinito per descrivere la modalità di riempimento della forma. È quindi possibile usare gli attributi di proprietà del `<fill>` sottoelemento per personalizzare l'effetto di riempimento, ad esempio [riempimento sfumato](#gradient-fill), [riempimento schema](#pattern-fill), riempimento [immagine](#picture-fill).

In questo argomento

-   [Riempimento sfumatura](#gradient-fill)
-   [Riempimento modello](#pattern-fill)
-   [Riempimento immagine](#picture-fill)

## <a name="gradient-fill"></a>Riempimento sfumatura

Per disegnare una forma con riempimento sfumato, è possibile impostare l'attributo della proprietà **Type** del `<fill>` sottoelemento su "gradiente" o "gradientRadial", quindi specificare altri attributi di proprietà del `<fill>` sottoelemento, ad esempio **Method**, **color2**, **Focus** e **Angle**.

**Esempi:**

Per creare una forma con riempimento sfumato orizzontalmente, è possibile impostare l'attributo della proprietà **Type** su "gradiente", come illustrato nella rappresentazione la seguente:

![horizontal1.gif (3055 byte)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Se si modifica l'attributo della proprietà **FillColor** della forma, la forma viene riempita con una sfumatura con un colore diverso. È possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del `<fill>` sottoelemento. Ad esempio, per creare una forma con riempimento sfumato in due colori, è possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del `<fill>` sottoelemento, come illustrato nella rappresentazione la seguente:

![horizontal2.gif (3127 byte)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




È possibile impostare l'attributo della proprietà del **Metodo** su "Linear" o "Sigma" o "any" o "None". L'effetto della sfumatura è leggermente diverso. Inoltre, è possibile utilizzare l'attributo della proprietà **Angle**,**Focus**,**focussize** o **focusposition** per modificare il modo in cui la sfumatura diventa.

**Esempi:**

 

Per creare una forma con riempimento sfumato verticalmente, è possibile impostare l'attributo della proprietà Angle su Angle = "-90", come illustrato nella rappresentazione la seguente:

![vertical1.gif (3836 byte)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dalla diagonale verso l'alto, è possibile impostare l'attributo della proprietà **Angle** su Angle = "-135", come illustrato nella rappresentazione la seguente:

![dialgonalup1.gif (5816 byte)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dalla diagonale verso il basso, è possibile impostare l'attributo della proprietà **Angle** su Angle = "-45", come illustrato nella rappresentazione la seguente:

![diagonaldown1.gif (5753 byte)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dal centro, è possibile specificare `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , come illustrato nella rappresentazione la seguente:

![fromcenter1.gif (4598 byte)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="pattern-fill"></a>Riempimento modello

Per disegnare una forma con riempimento a modelli, è possibile impostare l'attributo della proprietà **Type** del `<fill>` sottoelemento su "pattern", quindi specificare altri attributi di proprietà del `<fill>` sottoelemento, ad esempio **src** e **color2**.

**Esempi:**

Per creare una forma riempita con un'immagine del modello, è possibile specificare l'attributo della proprietà **Type** su "pattern" e puntare l'attributo della proprietà **src** al percorso del file di immagine del modello, come illustrato nella rappresentazione la seguente:

![pattern1.gif (872 byte)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Se si punta l'attributo della proprietà **src** a un file di modello diverso, è possibile creare una forma con un modello diverso. Inoltre, è possibile modificare il colore specificando un valore diverso per l'attributo della proprietà **FillColor** o **color2** , come illustrato nella rappresentazione la seguente:

![pattern2.gif (831 byte)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="picture-fill"></a>Riempimento immagine

Per disegnare una forma con riempimento immagine, è possibile impostare l'attributo della proprietà **Type** del `<fill>` sottoelemento su "frame", quindi specificare altri attributi di proprietà del `<fill>` sottoelemento, ad esempio **src** e **color2**.

**Esempi:**

Per creare una forma compilata con un file di immagine, è possibile specificare l'attributo della proprietà **Type** su "frame", quindi puntare l'attributo della proprietà **src** al percorso del file di immagine, come illustrato nella rappresentazione la seguente:

![picture1.gif (8496 byte)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




È possibile creare facilmente una forma riempita con un'immagine diversa puntando l'attributo della proprietà **src** a un altro file.

Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 