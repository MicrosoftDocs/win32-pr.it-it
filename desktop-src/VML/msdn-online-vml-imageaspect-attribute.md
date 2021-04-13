---
title: Attributo ImageAspect di la
description: Attributo ImageAspect di la
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338118"
---
# <a name="vml-imageaspect-attribute"></a>Attributo ImageAspect di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il modo in cui verranno mantenute le proporzioni dell'immagine del tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v:

elemento *imageaspect = "* expression *" >*

**Sintassi dello script**

Element *. imageaspect = "* Expression *"*

*=* elemento Expression *. imageaspect*

**Osservazioni:**

I possibili valori sono:



| Valore   | Descrizione                                |
|---------|--------------------------------------------|
| Ignora  | Ignorare i problemi di aspetto.                      |
| AtLeast | L'immagine è almeno uguale a **ImageSize**. |
| AtMost  | L'immagine non è maggiore di **ImageSize**.     |



 

In ogni caso, l'attributo **ImageSize** verrà regolato in modo da mantenere l'aspetto dell'immagine.

*Attributo standard la*

**Esempio**

L'immagine del tratto sarà almeno uguale alla dimensione dell'immagine.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 