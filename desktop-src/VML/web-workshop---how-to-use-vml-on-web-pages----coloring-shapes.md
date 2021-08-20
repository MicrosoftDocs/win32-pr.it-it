---
title: Colorazione delle forme
description: Questo articolo descrive la colorazione delle forme in VML, una funzionalità deprecata a Windows Internet Explorer 9.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web workshop, colorazione di forme
- progettazione di pagine Web, colorazione di forme
- Vector Markup Language (VML), colorazione di forme
- VML (Vector Markup Language),colorazione delle forme
- grafica vettoriale, colorazione di forme
- forme VML, colorazione
- colorazione di forme
- Vector Markup Language (VML), nomi di colore delle parole chiave
- VML (Vector Markup Language),nomi dei colori delle parole chiave
- grafica vettoriale, nomi di colore delle parole chiave
- nomi di colore delle parole chiave
- Vector Markup Language (VML),RGB triplets
- VML (Vector Markup Language),triplette RGB
- grafica vettoriale, triplette RGB
- Triplette RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edd8b067f1e3648d2b69f473c02c59392a10b5716afea74b8f7b0c9d093989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057049"
---
# <a name="coloring-shapes"></a>Colorazione delle forme

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Come accennato nelle sezioni precedenti, è possibile usare "rosso" per rappresentare un colore in rosso, "blu" per rappresentare un colore in blu e così via. In questo argomento verrà illustrato come disegnare forme con qualsiasi colore.

VML estende la sintassi dei colori HTML e CSS. Quando il tipo di attributo di un elemento VML è il colore, ad esempio [](#keyword-color-name) **fillcolor** e **strokecolor,** è possibile esprimere il colore usando un nome di colore per parola chiave o una tripletta [RGB.](#rgb-triplet)

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="keyword-color-name"></a>Nome colore parola chiave

HTML 4.0 definisce un elenco di nomi di colori delle parole chiave. Si tratta di acqua, nero, blu, fuchsia, grigio, verde, blu, maroon, viola, viola, rosso, silver, verde acqua, bianco e giallo. Il valore RGB per questi 16 colori è definito nella [specifica HTML 4.0.](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5)

Ad esempio, è possibile disegnare un rettangolo pieno di giallo specificando e assegnargli un contorno blu specificando , come illustrato nella rappresentazione `fillcolor="yellow"` `strokecolor="blue"` VML seguente:

![color1.gif (305 byte)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="rgb-triplet"></a>Tripletta RGB

Se il colore non è un [nome](#keyword-color-name)di colore della parola chiave, è possibile esprimere il colore come tripletta decimale RGB o tripletta esadecimale RGB. Con le triplette RGB, è possibile specificare i valori per i componenti rosso, verde e blu del colore, impostando ogni componente su un valore compreso tra 0 e 255 in decimale o da 00 a FF in formato esadecimale.

Ad esempio, è possibile creare un rettangolo riempito con un colore personalizzato con un valore RGB pari a 253, 249, 186 in decimal specificando o , come illustrato nella rappresentazione `fillcolor="rgb(253,249, 186)"` `fillcolor="#FDF9BA"` VML seguente. In formato esadecimale, il valore 253 diventa FD, 249 diventa F9 e 186 diventa BA.

![color2.gif (305 byte)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Se il RGB in formato esadecimale ha un modello come XXYYZZ, è possibile abbreviare il valore in XYZ. Ad esempio, " \# 66FF99" può essere scritto come " \# 6F9".

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

In VML è possibile rappresentare un colore in uno dei formati seguenti:

1.  fillcolor="blue"
2.  fillcolor="rgb(0,0,255)"
3.  fillcolor=" \# 0000ff"

 

 