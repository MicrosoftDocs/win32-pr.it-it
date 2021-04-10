---
title: Elemento Shadow la
description: Elemento Shadow la
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963122"
---
# <a name="vml-shadow-element"></a>Elemento Shadow la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un'ombreggiatura per una forma.

Gli attributi seguenti modificano un'ombreggiatura.



| Attributo                                          | Descrizione                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Colore](color-attribute--shadow--vml.md)          | Definisce il colore di un'ombreggiatura.                     |
| [Color2](color2-attribute--shadow--vml.md)        | Definisce il secondo colore di un'ombreggiatura.              |
| [ID](id-attribute--shadow--vml.md)                | Specifica l'identificatore univoco di un'ombreggiatura.       |
| [Matrice](matrix-attribute--shadow--vml.md)        | Definisce la trasformazione della prospettiva di un'ombreggiatura.     |
| [Nascosto](msdn-online-vml-obscured-attribute.md) | Determina se l'ombreggiatura è trasparente.      |
| [Offset](offset-attribute--shadow--vml.md)        | Definisce la distanza con cui l'ombreggiatura si estende oltre la forma. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Definisce un secondo offset.                           |
| [Sì](on-attribute--shadow--vml.md)                | Determina se viene visualizzata un'ombreggiatura.          |
| [Opacità](opacity-attribute--shadow--vml.md)      | Determina la trasparenza di un'ombreggiatura.           |
| [Origine](origin-attribute--shadow--vml.md)        | Definisce il centro dell'ombreggiatura.                  |
| [Tipo](type-attribute--shadow--vml.md)            | Specifica il tipo di ombreggiatura.                      |



 

**Osservazioni:**

Questo elemento deve essere definito all'interno di un elemento [Shape](shape-element--vml.md) .

Inoltre, l'attributo [on](on-attribute--shadow--vml.md) deve essere impostato su **true**.

Di seguito è riportato il codice minimo necessario per produrre un'ombreggiatura.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



L'ombreggiatura potrebbe non essere nota a meno che non si aumentino i valori di [offset](offset-attribute--shadow--vml.md) , poiché l'offset predefinito è 2PT, 2Pt.

**esempi**

-   [Esempio di ombreggiatura semplice](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Esempio di ombreggiatura dinamica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 