---
title: Attributo Opacity (Stroke)(VML)
description: Attributo Opacity (Stroke)(VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f457ee73ffdccd589f5ab3b4d89c5ce4c05f871a71572c1f04b2ddef5de4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596772"
---
# <a name="opacity-attribute-strokevml"></a>Attributo Opacity (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la quantità di trasparenza di un tratto. Proprietà di lettura/scrittura. **VgFraction**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *elemento* opacity=" *espressione* ">

**Sintassi dello script**

*elemento* .opacity="*expression*"

*expression* = *opacità* dell'elemento

**Osservazioni:**

Il valore predefinito è 1,0.

*Attributo standard VML*

**Esempio**

Il tratto è trasparente al 50%.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 