---
title: Ridimensionamento delle forme
description: Ridimensionamento delle forme
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Workshop Web, ridimensionamento delle forme
- progettazione di pagine Web, ridimensionamento di forme
- Vector Markup Language (VML), ridimensionamento delle forme
- VML (Vector Markup Language),ridimensionamento delle forme
- grafica vettoriale, ridimensionamento delle forme
- forme VML, ridimensionamento
- ridimensionamento di forme
- Vector Markup Language (VML), forme di ridimensionamento
- VML (Vector Markup Language), ridimensionamento delle forme
- grafica vettoriale, ridimensionamento delle forme
- forme VML, ridimensionamento
- ridimensionamento di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc7f62d802548ef1bc19aabf33c886c5b826098ae1280a9dd0b69413c9a61aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057033"
---
# <a name="scaling-shapes"></a>Ridimensionamento delle forme

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Si è appreso come disegnare e colorare forme in una pagina Web usando VML. In questo argomento verrà illustrato come ridimensionare le forme in base alle dimensioni desiderate.

VML usa la stessa sintassi definita nella sezione [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) (Dettagli modello di rendering visivo) della specifica [CSS2](https://www.w3.org/TR/PR-CSS2/) per specificare le dimensioni della casella contenitore in modo che il rendering (disegnato) del contenuto di una forma sia eseguito all'interno della casella contenitore. È possibile usare gli **attributi di stile larghezza** **e** altezza per definire le dimensioni della casella contenitore.

Ad esempio, se si disegna un ovale e si specifica **style**='width:75pt;height:100pt', l'ovale verrà disegnato all'interno di una casella contenitore di dimensioni pari a 75 punti (larghezza) di 100 punti (altezza), come illustrato nell'immagine seguente:

![oval1.gif (660 byte)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





Se si modifica la dimensione in **style**='width:120pt;height:140pt', l'ovale diventa più grande perché viene ridimensionato all'interno della nuova casella contenitore con una dimensione di 120 punti (larghezza) di 140 punti (altezza), come illustrato nell'immagine seguente:

![oval2.gif (966 byte)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





Se si modifica la dimensione in **style**='width:60pt;height:40pt', l'ovale diventa più piccolo perché viene ridimensionato all'interno della nuova casella contenitore con una dimensione di 60 punti (larghezza) di 40 punti (altezza), come illustrato nell'immagine seguente:

![oval3.gif (394 byte)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 