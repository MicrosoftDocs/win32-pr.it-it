---
title: Attributo VML ImageAlignShape
description: Attributo VML ImageAlignShape
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86090936556ba8a4f022024f292293b396d953d46962423a222b172adc2a15f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600469"
---
# <a name="vml-imagealignshape-attribute"></a>Attributo VML ImageAlignShape

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina l'allineamento dell'immagine del tratto. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v:

element *imagealignshape="* expression *">*

**Sintassi dello script**

element *.imagealignshape="* expression *"*

Elemento *=* expression *.imagealignshape*

**Osservazioni:**

Se **True,** allineare l'immagine alla forma, altrimenti allineare l'immagine alla finestra. Il valore predefinito è **True**.

*Attributo VML Standard*

**Esempio**

L'immagine è allineata alla finestra.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 