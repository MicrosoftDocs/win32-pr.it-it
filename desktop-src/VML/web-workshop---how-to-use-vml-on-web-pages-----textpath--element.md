---
title: Uso dell'elemento Textpath
description: Uso dell'elemento Textpath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Workshop Web, elemento textpath
- progettazione di pagine Web, elemento textpath
- Vector Markup Language (VML),elemento textpath
- VML (Vector Markup Language),elemento textpath
- grafica vettoriale, elemento textpath
- elemento textpath
- Elementi VML, textpath
- Forme VML, elemento textpath
- Vector Markup Language (VML), disegno di testo
- VML (Vector Markup Language),disegno di testo
- grafica vettoriale, disegno di testo VML
- creazione di testo
- forme VML, disegno di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5db3b76d0c4ad2e56c59cfcf6dd39a2af51317b63ee190f47d794933282b5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056979"
---
# <a name="using-the-textpath-element"></a>Uso dell'elemento Textpath

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento verrà illustrato come usare l'elemento `<textpath>` per disegnare testo con vari stili.

È possibile inserire il `<textpath>` sotto-elemento all'interno `<shape>` di o per disegnare `<shapetype>` testo. È quindi possibile usare gli attributi della proprietà del `<textpath>` sotto-elemento per personalizzare il testo. È anche possibile usare `<formulas>` il sotto-elemento per definire la struttura del testo.

Ad esempio, per creare il testo mostrato nell'immagine seguente, è possibile digitare la rappresentazione VML seguente. Si noti che si usa `<shapetype>` l'elemento per definire un prototipo per la struttura del testo. Viene quindi creata un'istanza di due forme dallo stesso tipo di forma. È possibile modificare semplicemente **l'attributo della** proprietà stringa per visualizzare testo diverso.

![shape1 \-1.gif (4898 byte)](images/shape1-1t.gif)

![shape1 \-2.gif (2789 byte)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 