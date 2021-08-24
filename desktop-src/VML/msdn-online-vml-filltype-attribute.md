---
title: Attributo FillType VML
description: Attributo FillType VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0264fe6cd8cd3dfb7592aea25ef855fda01632647b23f0ab2cffe84c4c504918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680801"
---
# <a name="vml-filltype-attribute"></a>Attributo FillType VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce il tipo di riempimento usato per lo sfondo di un tratto. Proprietà di lettura/scrittura. **VgFillType**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* filltype=" *expression* ">

**Sintassi dello script**

*element* .filltype="*expression*"

*expression* = *elemento*.filltype

**Osservazioni:**

I possibili valori sono:



| Dashstyle | Descrizione                                    |
|-----------|------------------------------------------------|
| Tinta unita     | Il motivo di riempimento è a tinta unita. Valore predefinito.      |
| Tile      | L'immagine di riempimento è affiancata.                       |
| Modello   | L'immagine di riempimento viene estesa in modo da formare un motivo. |
| Frame     | L'immagine di riempimento diventa un bordo per la forma. |



 

*Attributo standard VML*

**Esempio**

Il tratto della forma ha una trama affiancata creata dall'cylinder.gif immagine.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 