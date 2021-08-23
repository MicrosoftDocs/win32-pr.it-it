---
title: Uso dell'elemento Fill
description: Questo articolo descrive l'uso dell'elemento Fill di VML, una funzionalità deprecata a Windows Internet Explorer 9.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Workshop Web, elemento fill
- progettazione di pagine Web, elemento fill
- Vector Markup Language (VML), elemento fill
- VML (Vector Markup Language),elemento fill
- grafica vettoriale, elemento fill
- fill - elemento
- elementi VML, riempimento
- Forme VML, elemento fill
- Vector Markup Language (VML), riempimento sfumato
- VML (Vector Markup Language),riempimento sfumato
- grafica vettoriale, riempimento sfumato
- Forme VML, riempimento sfumato
- forme con riempimento sfumato
- Vector Markup Language (VML), riempimento a motivo
- VML (Vector Markup Language),riempimento a motivo
- grafica vettoriale, riempimento a motivo
- Forme VML, riempimento a motivo
- forme con motivo pieno
- Vector Markup Language (VML), riempimento immagine
- VML (Vector Markup Language),riempimento immagine
- grafica vettoriale, riempimento immagine
- Forme VML, riempimento immagine
- Forme con riempimento a immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f6b3e0c92989e037ebf9b95b7bd726134b9099dd5d3755ff4588f7e970586c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057265"
---
# <a name="using-the-fill-element"></a>Uso dell'elemento Fill

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Come si è appreso, è possibile usare l'attributo della proprietà **fillcolor** di un elemento forma predefinito, ad esempio , , , , , , , per specificare il colore usato per riempire la `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. In questo argomento verrà illustrato come disegnare una forma riempita con effetti più avanzati.

È possibile inserire il sotto-elemento all'interno di , o o qualsiasi elemento di forma predefinito per descrivere `<fill>` `<shape>` come riempire la `<shapetype>` forma. È quindi possibile usare gli attributi della proprietà del sotto-elemento per personalizzare l'effetto di riempimento, ad esempio il riempimento `<fill>` [sfumato,](#gradient-fill)il [riempimento](#pattern-fill)a motivo, il [riempimento immagine.](#picture-fill)

In questo argomento

-   [Riempimento sfumato](#gradient-fill)
-   [Riempimento a motivo](#pattern-fill)
-   [Riempimento immagine](#picture-fill)

## <a name="gradient-fill"></a>Riempimento sfumato

Per disegnare una forma con riempimento sfumato, è possibile impostare l'attributo della proprietà type del sotto-elemento su "gradient"  o `<fill>` "gradientRadial" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio il metodo , color2 , lo stato attivo e `<fill>` **l'angolo**.   

**Esempi:**

Per creare una forma con riempimento sfumato  orizzontalmente, è possibile impostare l'attributo della proprietà type su "gradient", come illustrato nella rappresentazione VML seguente:

![horizontal1.gif (3055 byte)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Se si modifica **l'attributo della** proprietà fillcolor della forma, la forma viene riempita con sfumatura con un colore diverso. È possibile aggiungere un secondo colore specificando **l'attributo della proprietà color2** del `<fill>` sotto-elemento. Ad esempio, per creare una forma con riempimento sfumato in due colori, è possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del sotto-elemento, come illustrato nella rappresentazione `<fill>` VML seguente:

![horizontal2.gif (3127 byte)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




È possibile impostare **l'attributo** della proprietà del metodo su "linear" o "sigma" o "any" o "none". L'effetto della sfumatura è leggermente diverso. È anche possibile usare l'attributo della proprietà **angle,****focus,****focussize** o **focusposition** per modificare l'andamenti della sfumatura.

**Esempi:**

 

Per creare una forma con riempimento sfumato verticalmente, è possibile impostare l'attributo della proprietà angle su angle="-90", come illustrato nella rappresentazione VML seguente:

![vertical1.gif (3836 byte)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dalla diagonale che si sposta verso l'alto, è possibile impostare l'attributo della proprietà **angle** su angle="-135", come illustrato nella rappresentazione VML seguente:

![dialgonalup1.gif (5816 byte)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dalla diagonale che si sposta verso il basso, è possibile impostare l'attributo della proprietà **angle** su angle="-45", come illustrato nella rappresentazione VML seguente:

![diagonaldown1.gif (5753 byte)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dal centro, è possibile specificare `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , come illustrato nella rappresentazione VML seguente:

![fromcenter1.gif (4598 byte)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="pattern-fill"></a>Riempimento a motivo

Per disegnare una forma con motivo pieno, è possibile impostare l'attributo della proprietà type del sotto-elemento su "pattern" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio  src e `<fill>` `<fill>` **color2.** 

**Esempi:**

Per creare una forma riempita con un'immagine  del criterio, è possibile specificare l'attributo della proprietà type su "pattern" e puntare l'attributo della proprietà **src** alla posizione del file di immagine del criterio, come illustrato nella rappresentazione VML seguente:

![pattern1.gif (872 byte)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Se si punta **l'attributo della** proprietà src a un file di criteri diverso, è possibile creare una forma riempita con un modello diverso. È anche possibile modificare il colore specificando un valore diverso per l'attributo della proprietà **fillcolor** o **color2,** come illustrato nella rappresentazione VML seguente:

![pattern2.gif (831 byte)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="picture-fill"></a>Riempimento immagine

Per disegnare una forma piena di immagine, è possibile impostare l'attributo della proprietà type del sotto-elemento su "frame" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio  src e `<fill>` `<fill>` **color2.** 

**Esempi:**

Per creare una forma riempita con un file  di immagine, è possibile specificare l'attributo della proprietà type su "frame" e quindi puntare l'attributo della proprietà **src** alla posizione del file di immagine, come illustrato nella rappresentazione VML seguente:

![picture1.gif (8496 byte)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




È possibile creare facilmente una forma riempita con un'immagine diversa puntando l'attributo della proprietà **src** a un altro file.

Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 