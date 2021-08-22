---
title: Attributo Src (Stroke)(VML)
description: Attributo Src (Stroke)(VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bc71d7a36ee944a2352cde6bfa1ef33f0b5c480d78c7aada751ea67db9ca7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596627"
---
# <a name="src-attribute-strokevml"></a>Attributo Src (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'immagine di origine da caricare per un riempimento del tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* src=" *expression* ">

**Sintassi dello script**

*element* .src="*expression*"

*expression* = *elemento*.src

**Osservazioni:**

URL di un'immagine da caricare per i riempimenti immagine e motivo. Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine. Se questo attributo viene visualizzato da solo, ad esempio senza **HRef** o **Title,** l'immagine è collegata.

*Attributo VML Standard*

**Esempio**

Il tratto viene creato con l'immagine specificata dal file cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 