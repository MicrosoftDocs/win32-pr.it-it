---
title: Attributo VML ImageAspect
description: Attributo VML ImageAspect
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f67d715d5cd10d36b4e8e7e32f939aeeef2bbdd894aba9da5a069ef03f0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600354"
---
# <a name="vml-imageaspect-attribute"></a>Attributo VML ImageAspect

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce come verranno mantenute le proporzioni dell'immagine del tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v:

element *imageaspect="* expression *">*

**Sintassi dello script**

element *.imageaspect="* expression *"*

Elemento *=* expression *.imageaspect*

**Osservazioni:**

I possibili valori sono:



| Valore   | Descrizione                                |
|---------|--------------------------------------------|
| Ignora  | Ignorare i problemi relativi all'aspetto.                      |
| Atleast | L'immagine è grande almeno quanto **ImageSize.** |
| AtMost  | L'immagine non è più grande **di ImageSize.**     |



 

In ogni caso, **l'attributo ImageSize** verrà regolato per mantenere l'aspetto dell'immagine.

*Attributo standard VML*

**Esempio**

L'immagine del tratto sarà grande almeno quanto le dimensioni dell'immagine.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 