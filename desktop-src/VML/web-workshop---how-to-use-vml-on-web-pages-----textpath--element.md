---
title: Utilizzo dell'elemento TextPath
description: Utilizzo dell'elemento TextPath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Web Workshop, elemento TextPath
- progettazione di pagine Web, elemento TextPath
- Vector Markup Language (la), elemento TextPath
- LA (Vector Markup Language), elemento TextPath
- grafica vettoriale, elemento TextPath
- elemento TextPath
- Elementi la, TextPath
- Forme la, elemento TextPath
- Vector Markup Language (la), disegno del testo
- LA (Vector Markup Language), disegno di testo
- grafica vettoriale, disegno del testo la
- creazione di testo
- LA forme, disegno del testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118374"
---
# <a name="using-the-textpath-element"></a>Utilizzo dell'elemento TextPath

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento verrà illustrato come utilizzare l' `<textpath>` elemento per disegnare testo con diversi stili.

È possibile inserire il `<textpath>` sottoelemento all'interno `<shape>` o `<shapetype>` per creare il testo. È quindi possibile usare gli attributi di proprietà del `<textpath>` sottoelemento per personalizzare il testo. È anche possibile usare il `<formulas>` sottoelemento per definire il contorno del testo.

Per creare, ad esempio, il testo illustrato nell'immagine seguente, è possibile digitare la rappresentazione la riportata di seguito. Si noti che viene usato l' `<shapetype>` elemento per definire un prototipo per il contorno del testo. Viene quindi creata un'istanza di due forme dallo stesso TipoForma. È possibile modificare semplicemente l'attributo della proprietà **stringa** per visualizzare testo diverso.

![\-1.gif Shape1 (4898 byte)](images/shape1-1t.gif)

![\-2.gif Shape1 (2789 byte)](images/shape1-2t.gif)


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





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 