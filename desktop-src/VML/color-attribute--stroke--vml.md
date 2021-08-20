---
title: Attributo Color (Stroke)(VML)
description: Attributo Color (Stroke)(VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17b3dd30d95765c98ec754526349b2bdc274696112043065fa7ddc7d894b582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125371"
---
# <a name="color-attribute-strokevml"></a>Attributo Color (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce il colore di un tratto. Proprietà di lettura/scrittura. **VgColor**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* color=" *expression* ">

**Sintassi dello script**

*element* .color="*expression*"

*expression* = *elemento*.color

**Osservazioni:**

Esegue l'override **dell'attributo StrokeColor** di una forma. Il valore predefinito è **nero.**

*Attributo standard VML*

**Esempio**

La forma ha un colore del tratto **verde,** non **rosso.**


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 