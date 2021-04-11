---
title: Colori delle forme
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Workshop Web, forme colorazione
- progettazione di pagine Web, colorazione di forme
- Vector Markup Language (la), forme colorazione
- LA (Vector Markup Language), forme colorazione
- grafica vettoriale, forme colorazione
- Forme la, colorazione
- colori delle forme
- Vector Markup Language (la), nomi dei colori delle parole chiave
- LA (Vector Markup Language), nomi di colori delle parole chiave
- grafica vettoriale, nomi dei colori delle parole chiave
- nomi dei colori delle parole chiave
- Vector Markup Language (la), triple RGB
- LA (Vector Markup Language), triple RGB
- grafica vettoriale, triplette RGB
- Triplette RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047047"
---
# <a name="coloring-shapes"></a>Colori delle forme

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Come indicato nelle sezioni precedenti, è possibile usare "Red" per rappresentare un colore in rosso, "blu" per rappresentare un colore in blu e così via. In questo argomento verrà illustrato come creare forme nei colori desiderati.

LA estende la sintassi di colore HTML e CSS. Quando il tipo di attributo di un elemento la è color, ad esempio **FillColor** e **StrokeColor** , è possibile esprimere il colore usando un [nome di colore della parola chiave](#keyword-color-name) o una [tripletta RGB](#rgb-triplet).

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="keyword-color-name"></a>Nome colore parola chiave

HTML 4,0 definisce un elenco di nomi di colori delle parole chiave. Sono Aqua, black, Blue, fucsia, grigio, verde, lime, Maroon, Navy, olive, Purple, Red, Silver, alzavola, White e Yellow. Il valore RGB per questi 16 colori è definito nella [specifica HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .

Ad esempio, è possibile disegnare un rettangolo riempito con il giallo specificando `fillcolor="yellow"` e assegnargli un contorno blu specificando `strokecolor="blue"` , come illustrato nella rappresentazione la seguente:

![color1.gif (305 byte)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="rgb-triplet"></a>Tripletta RGB

Se il colore non è un [nome di colore di parola chiave](#keyword-color-name), è possibile esprimere il colore come una tripletta decimale RGB o una tripletta esadecimale RGB. Con le triplette RGB è possibile specificare i valori per i componenti rosso, verde e blu del colore, impostando ogni componente su un valore compreso tra 0 e 255 in decimale oppure 00 con FF in formato esadecimale.

È ad esempio possibile creare un rettangolo con un colore personalizzato con un valore RGB 253, 249, 186 in Decimal specificando `fillcolor="rgb(253,249, 186)"` o `fillcolor="#FDF9BA"` , come illustrato nella rappresentazione la seguente. In esadecimale, il valore 253 diventa FD, 249 diventa F9 e 186 diventa BA.

![color2.gif (305 byte)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Se l'oggetto RGB in formato esadecimale ha un modello, ad esempio XXYYZZ, è possibile abbreviare l'oggetto con XYZ. Ad esempio, " \# 66FF99" può essere scritto come " \# 6F9".

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

In la è possibile rappresentare un colore in uno dei formati seguenti:

1.  FillColor = "blu"
2.  FillColor = "RGB (0, 0255)"
3.  FillColor = " \# 0000FF"

 

 