---
title: Elemento asimmetria la
description: Elemento asimmetria la
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e317d03fc0bbef361df56282bec55ea2a9e708f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473155"
---
# <a name="vml-skew-element"></a>Elemento asimmetria la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una asimmetria per una forma.

Gli attributi seguenti modificano una asimmetria.



| Attributo                                 | Descrizione                                    |
|-------------------------------------------|------------------------------------------------|
| [EXT](ext-attribute--skew--vml.md)       | Definisce la modalità di visualizzazione di una asimmetria.           |
| [ID](id-attribute--skew--vml.md)         | Definisce un identificatore univoco per una asimmetria.        |
| [Matrice](matrix-attribute--skew--vml.md) | Definisce una trasformazione della prospettiva per una asimmetria.    |
| [Offset](offset-attribute--skew--vml.md) | Definisce l'offset di una asimmetria.                  |
| [Sì](on-attribute--skew--vml.md)         | Determina se verrà visualizzata l'asimmetria. |
| [Origine](origin-attribute--skew--vml.md) | Determina l'origine di una asimmetria.               |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Inoltre, gli attributi [Matrix](matrix-attribute--skew--vml.md) e [on](on-attribute--skew--vml.md) devono essere impostati su **true**.

Di seguito è riportato il codice minimo necessario per produrre un'asimmetria.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



L'elemento **asimmetria** è un'estensione Microsoft Office di la.

**esempi**

-   [Esempio di asimmetria semplice](/previous-versions/bb229482(v=vs.85))
-   [Esempio di asimmetria dinamica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 