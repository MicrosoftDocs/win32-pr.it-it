---
title: Uso dell'elemento Fill
description: Questo articolo descrive l'uso dell'elemento Fill di VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web workshop, elemento fill
- progettazione di pagine Web, elemento fill
- Vector Markup Language (VML), elemento fill
- VML (Vector Markup Language),elemento fill
- grafica vettoriale, elemento fill
- elemento fill
- elementi VML, riempimento
- Forme VML, elemento fill
- Vector Markup Language (VML), riempimento sfumato
- VML (Vector Markup Language),riempimento sfumato
- grafica vettoriale, riempimento sfumato
- Forme VML, riempimento sfumato
- Forme con riempimento sfumato
- Vector Markup Language (VML), riempimento a motivo
- VML (Vector Markup Language),riempimento a motivo
- grafica vettoriale, riempimento a motivo
- Forme VML, riempimento a motivo
- forme con riempimento a motivo
- Vector Markup Language (VML), riempimento immagine
- VML (Vector Markup Language),riempimento immagine
- grafica vettoriale, riempimento immagine
- Forme VML, riempimento immagine
- Forme con riempimento a immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407794"
---
# <a name="using-the-fill-element"></a>Uso dell'elemento Fill

Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Come si è appreso, è possibile usare l'attributo della proprietà **fillcolor** di un elemento forma predefinito, ad esempio , , , , , per specificare il colore usato per riempire `<oval>` la `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma. In questo argomento verrà illustrato come disegnare una forma riempita con effetti più avanzati.

È possibile inserire il sotto-elemento all'interno di , o o qualsiasi elemento di forma predefinito per descrivere `<fill>` `<shape>` come riempire la `<shapetype>` forma. È quindi possibile usare gli attributi della proprietà del sotto-elemento per personalizzare l'effetto di riempimento, ad esempio il riempimento sfumato, il riempimento a `<fill>` [motivi,](#pattern-fill)il [riempimento immagine.](#picture-fill) [](#gradient-fill)

In questo argomento

-   [Riempimento sfumato](#gradient-fill)
-   [Riempimento a motivo](#pattern-fill)
-   [Riempimento immagine](#picture-fill)

## <a name="gradient-fill"></a>Riempimento sfumato

Per disegnare una forma con riempimento sfumato, è possibile impostare l'attributo della proprietà type del sotto-elemento su "gradient" o  `<fill>` "gradientRadial" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio `<fill>` **method**, **color2**, **focus** e **angle**.

**Esempi:**

Per creare una forma con riempimento sfumato  orizzontalmente, è possibile impostare l'attributo della proprietà type su "gradient", come illustrato nella rappresentazione VML seguente:

![horizontal1.gif (3055 byte)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Se si modifica **l'attributo della** proprietà fillcolor della forma, la forma viene riempita con una sfumatura con un colore diverso. È possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del `<fill>` sotto-elemento. Ad esempio, per creare una forma con riempimento sfumato in due colori, è possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del sotto-elemento, come illustrato nella rappresentazione `<fill>` VML seguente:

![horizontal2.gif (3127 byte)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




È possibile impostare **l'attributo** della proprietà del metodo su "linear" o "sigma" o "any" o "none". L'effetto della sfumatura è leggermente diverso. È anche possibile usare l'attributo della proprietà **angle,****focus,****focussize** o **focusposition** per modificare il modo in cui va la sfumatura.

**Esempi:**

 

Per creare una forma con riempimento sfumato verticalmente, è possibile impostare l'attributo della proprietà angle su angle="-90", come illustrato nella rappresentazione VML seguente:

![vertical1.gif (3836 byte)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dalla diagonale verso l'alto, è possibile impostare l'attributo della proprietà **angle** su angle="-135", come illustrato nella rappresentazione VML seguente:

![dialgonalup1.gif (5816 byte)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Per creare una forma con riempimento sfumato dalla diagonale verso il basso, è possibile impostare l'attributo della proprietà **angle** su angle="-45", come illustrato nella rappresentazione VML seguente:

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

Per disegnare una forma con riempimento a  motivo, è possibile impostare l'attributo della proprietà type del sotto-elemento su "pattern" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio src e `<fill>` `<fill>` **color2.** 

**Esempi:**

Per creare una forma riempita con un'immagine  modello, è possibile specificare l'attributo della proprietà type su "pattern" e puntare l'attributo della proprietà **src** alla posizione del file di immagine del modello, come illustrato nella rappresentazione VML seguente:

![pattern1.gif (872 byte)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Se si punta l'attributo della proprietà **src** a un file di criteri diverso, è possibile creare una forma riempita con un modello diverso. È anche possibile modificare il colore specificando un valore diverso per l'attributo della proprietà **fillcolor** o **color2,** come illustrato nella rappresentazione VML seguente:

![pattern2.gif (831 byte)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="picture-fill"></a>Riempimento immagine

Per disegnare una forma con riempimento a  immagine, è possibile impostare l'attributo della proprietà type del sotto-elemento su "frame" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio src e `<fill>` `<fill>` **color2.** 

**Esempi:**

Per creare una forma riempita con un file  di immagine, è possibile specificare l'attributo della proprietà type su "frame" e quindi puntare l'attributo della proprietà **src** al percorso del file di immagine, come illustrato nella rappresentazione VML seguente:

![picture1.gif (8496 byte)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




È possibile creare facilmente una forma riempita con un'immagine diversa puntando l'attributo della proprietà **src** a un altro file.

Per altre informazioni su questo elemento, vedere la specifica [VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 