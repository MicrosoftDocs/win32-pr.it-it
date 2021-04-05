---
title: Ridimensionamento di forme
description: Ridimensionamento di forme
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web Workshop, ridimensionamento delle forme
- progettazione di pagine Web, ridimensionamento delle forme
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727938"
---
# <a name="scaling-shapes"></a>Ridimensionamento di forme

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Si è appreso come creare e colorare forme in una pagina Web usando la. In questo argomento verrà illustrato come ridimensionare le forme con le dimensioni desiderate.

LA utilizza la stessa sintassi definita nella sezione [Dettagli del modello di rendering visivo](https://www.w3.org/TR/PR-CSS2/visudet.mdl) della [specifica CSS2](https://www.w3.org/TR/PR-CSS2/) per specificare le dimensioni della casella contenitore in modo che il contenuto di una forma venga sottoposto a rendering (tracciato) all'interno della casella contenitore. È possibile utilizzare gli attributi di stile **larghezza** e **altezza** per definire le dimensioni della casella contenitore.

Se ad esempio si disegna un ovale e si specifica **Style**=' width: 75pt; Height: 100PT ', l'ovale verrà disegnato all'interno di una casella contenitore con una dimensione di 75 punti (larghezza) di 100 punti (altezza), come illustrato nell'immagine seguente:

![oval1.gif (660 byte)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Se si modifica la dimensione in **Style**=' width: 120pt; Height: 140pt ', l'ovale diventa più grande perché viene ridimensionato all'interno della nuova casella contenitore con una dimensione di 120 punti (larghezza) per 140 punti (altezza), come illustrato nell'immagine seguente:

![oval2.gif (966 byte)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Se si modifica la dimensione in **Style**=' width: 60pt; Height: 40pt ', l'ovale diventa più piccolo perché viene ridimensionato all'interno della nuova casella contenitore con una dimensione di 60 punti (larghezza) per 40 punti (altezza), come illustrato nell'immagine seguente:

![oval3.gif (394 byte)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 