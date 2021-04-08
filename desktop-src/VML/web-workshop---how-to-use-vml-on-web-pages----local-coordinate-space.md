---
title: Utilizzo dello spazio delle coordinate locale
description: Utilizzo dello spazio delle coordinate locale
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Web Workshop, spazio delle coordinate locale
- progettazione di pagine Web, spazio delle coordinate locale
- Vector Markup Language (la), spazio delle coordinate locale
- LA (Vector Markup Language), spazio delle coordinate locale
- grafica vettoriale, spazio delle coordinate locale
- spazio delle coordinate locale
- Forme la, spazio delle coordinate locale
- Vector Markup Language (la), forme di raggruppamento
- LA (Vector Markup Language), forme di raggruppamento
- grafica vettoriale, forme raggruppamento
- LA forme, raggruppamento
- forme di raggruppamento
- Vector Markup Language (la), ridimensionamento delle forme
- LA (Vector Markup Language), ridimensionamento delle forme
- grafica vettoriale, forme di ridimensionamento
- LA forme, ridimensionamento
- ridimensionamento di forme
- Vector Markup Language (la), forme di ridimensionamento
- LA (Vector Markup Language), forme di ridimensionamento
- grafica vettoriale, forme di ridimensionamento
- Forme la, ridimensionamento
- ridimensionamento di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729735"
---
# <a name="using-local-coordinate-space"></a>Utilizzo dello spazio delle coordinate locale

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Come si è appreso, è possibile specificare gli attributi di stile **larghezza** e **altezza** per definire le dimensioni di una casella contenitore in cui verrà eseguito il rendering del contenuto di una forma o di un gruppo. In questo argomento verrà illustrato lo spazio delle coordinate locali e il modo in cui viene usato in la per ridimensionare le forme.

Se è stato richiesto di creare un rettangolo da un pollice a due pollici su una porzione di carta della griglia, la prima cosa da capire è dove iniziare (il punto di origine). Viene quindi illustrato come eseguire il mapping di un pollice alle celle del documento della griglia (la coordinata).

Analogamente, quando viene eseguito il rendering del contenuto di una forma o di un gruppo all'interno della casella contenitore in una pagina Web, è necessario definire il punto di origine e la coordinata. LA fornisce spazio delle coordinate locale per consentire a ogni forma o gruppo di definire il proprio punto di origine e coordinata. Se non si specifica uno spazio delle coordinate, verrà utilizzato quello predefinito. Per impostazione predefinita, l'origine inizia dall'angolo superiore sinistro della casella contenitore.

Ad esempio, la rappresentazione la per l'ovale rosso riportato di seguito non specifica gli attributi delle proprietà **coordsize** e **coordorigin** . Viene pertanto utilizzato uno spazio delle coordinate locale predefinito. La dimensione dell'ovale è 100 punti (larghezza) di 75 punti (altezza). È possibile ridimensionare l'ovale specificando una larghezza o un'altezza diversa, come illustrato nell'argomento [forme di scala](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .

![oval1.gif (627 byte)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





Quando la forma diventa più complessa o quando si desidera raggruppare più forme e ridimensionarle insieme, è necessario utilizzare la funzionalità spazio delle coordinate locale disponibile in la.

Per ogni forma o gruppo, è possibile usare gli attributi delle proprietà **coordsize** e **coordorigin** per definire lo spazio delle coordinate locali della forma o del gruppo. L'attributo **coordsize** specifica il numero di unità lungo la larghezza e l'altezza della casella contenitore. L'attributo **coordorigin** definisce la coordinata nell'angolo superiore sinistro della casella contenitore. Tutte le informazioni relative alla posizione, ad esempio larghezza, altezza, sinistra, superiore, percorso e così via, sono espresse in termini di unità nello spazio delle coordinate locali.

Ad esempio, come illustrato nella seguente rappresentazione la, `width: 100pt; height: 100pt;` definisce la dimensione della casella contenitore affinché la forma sia 100 punti per 100 punti.

![cord1.gif (836 byte)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` definisce la dimensione dello spazio delle coordinate locale affinché la forma sia 21600 unità per 21600 unità. Pertanto, un'unità nello spazio delle coordinate locale equivale a 1/216 punto.
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` definisce il contorno della forma come forma a rombo. Come è stato appreso, tutte le informazioni relative alla posizione, ad esempio larghezza, altezza, sinistra, superiore, percorso e così via, sono espresse in termini di unità nello spazio delle coordinate locali. Pertanto, 10800 in `<path>` significa 10800 unità, che equivale a 50 punti.

Quando si vuole ridimensionare questa forma a rombo, è sufficiente specificare una larghezza o un'altezza diversa, ovvero non è necessario modificare alcun valore in `<path>` . Per questa forma complicata, se non si utilizza la funzionalità spazio delle coordinate locale, sarà necessario modificare ogni valore in `<path>` ogni volta che si desidera ridimensionarlo.

È ad esempio possibile ridimensionare la forma a rombo semplicemente specificando una larghezza o un'altezza diversa, come illustrato nella seguente rappresentazione la:

![cord2.gif (1692 byte)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





È inoltre possibile utilizzare lo spazio delle coordinate locale nell' `<group>` elemento in modo che il contenuto di tutte le forme all'interno del gruppo venga ridimensionato in base alla stessa coordinata. Quindi, ogni volta che si desidera ridimensionare o spostare un gruppo di forme, è sufficiente modificare la larghezza e l'altezza oppure le impostazioni **coordsize** e **coordorigin** del gruppo.

Ad esempio, nella seguente rappresentazione la, `<v:group style='... width:200pt;height:200pt;'>` definisce la dimensione della casella contenitore affinché il gruppo sia 200 punti per 200 punti.

![cord3.gif (645 byte)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` definisce la dimensione dello spazio delle coordinate locale affinché il gruppo sia 1000 unità per 1000 unità. Pertanto, 1 unità nello spazio delle coordinate locale equivale a 1/5 punto.
-   `coordorigin="-500,-500"` definisce l'angolo superiore sinistro della casella contenitore in modo che sia "-500,-500". Pertanto, il sistema di coordinate all'interno della casella contenitore è compreso tra-500 e 500 lungo l'asse x e-500 a 500 lungo l'asse y. In altre parole, il centro della casella contenitore è "0, 0".
-   `<v:oval style='... width:400;height:300;'>` definisce la dimensione della casella che lo contiene per il rosso ovale da 400 unità (larghezza) per 300 unità (altezza). Poiché un'unità nello spazio delle coordinate locale equivale a 1/5 punti, la dimensione della casella contenitore per l'ovale rosso è 80 punti (larghezza) di 60 punti (altezza).

Analogamente, la dimensione della casella contenitore per il RoundRect verde è 50 punti (larghezza) per 40 punti (altezza).

Quando si vuole ridimensionare sia il rosso ovale che il RoundRect verde, è sufficiente modificare `<v:group style='... width:200pt;height:200pt;'>` . In questo modo, non è necessario modificare singolarmente le dimensioni delle due forme.

Se, ad esempio, si passa `<v:group style='... width:200pt;height:200pt;'>` a `<v:group style='... width:300pt;height:300pt;'>` , le forme diventano maggiori, come illustrato nell'immagine seguente:

![cord4.gif (943 byte)](images/cord4.gif)



Si noterà anche che le forme sono posizionate in modo diverso. Questo è dovuto al fatto che le forme vengono disegnate da "0,0", che si trova al centro della casella contenitore. Poiché la casella contenitore è più grande, viene spostato anche il centro della casella contenitore.

Se si passa `coordorigin="-500,-500"` a `coordorigin="0,0"` , come illustrato nell'immagine seguente, si noterà che il rosso ovale e il RoundRect verde sono spostati verso l'alto nella nuova posizione. Questo è dovuto al fatto che "0,0" individua ora nell'angolo superiore sinistro della casella contenitore.

![cord5.gif (648 byte)](images/cord5.gif)



È anche importante notare che la casella contenitore non stabilisce un'area di ridimensionamento. La grafica può essere disegnata all'esterno dei limiti della casella contenitore. La casella contenitore serve semplicemente per eseguire il mapping dello spazio delle coordinate locale allo spazio della pagina.

Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858382) .

 

 