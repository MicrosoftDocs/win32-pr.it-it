---
title: Utilizzo dell'elemento Path
description: Utilizzo dell'elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web Workshop, elemento Path
- progettazione di pagine Web, elemento Path
- Vector Markup Language (la), elemento Path
- LA (Vector Markup Language), elemento Path
- Vector graphics, elemento Path
- path-elemento
- Elementi la, percorso
- Forme la, elemento Path
- Vector Markup Language (la), personalizzazione delle strutture delle forme
- LA (Vector Markup Language), personalizzazione delle strutture delle forme
- grafica vettoriale, personalizzazione delle strutture delle forme
- LA forme, personalizzazione di strutture
- personalizzazione delle strutture delle forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729751"
---
# <a name="using-the-path-element"></a>Utilizzo dell'elemento Path

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Si è appreso che è possibile usare gli elementi di forma predefiniti di la, ad esempio `<oval>` ,, `<line>` `<polyline>` , `<curve>` , `<rect>` , e, `<roundrect>` `<arc>` per disegnare una forma. In questo argomento verrà illustrato come utilizzare il `<path>` sottoelemento per personalizzare il contorno di una forma.

È possibile inserire il `<path>` sottoelemento all'interno dell' `<shape>` `<shapetype>` elemento o. È quindi possibile usare gli attributi di proprietà del `<path>` sottoelemento per personalizzare il contorno della forma.

Per disegnare la forma personalizzata illustrata nell'immagine seguente, ad esempio, è possibile usare il `<path>` sottoelemento per definire il contorno della forma, come illustrato nella rappresentazione la seguente:

![shape1.gif (1301 byte)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   I valori `m 8,65` indicano che il disegno inizia in corrispondenza del punto (8, 65).
-   I valori `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicano che una linea retta inizia in corrispondenza del punto corrente (8, 65) e termina in corrispondenza del punto specificato (72, 65), che diventa il nuovo punto corrente. Una nuova riga inizia in corrispondenza del punto corrente (72, 65) e termina in corrispondenza del punto specificato, che diventa il nuovo punto corrente e così via, fino al punto finale (60, 100).
-   `x` indica che il percorso si chiuderà con una linea retta che inizia in corrispondenza del punto corrente (60, 100) e termina in corrispondenza del punto originale (8, 65).
-   `e` indica l'arresto del disegno.

Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 