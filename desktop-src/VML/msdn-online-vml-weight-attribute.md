---
title: Attributo la Weight
description: Attributo la Weight
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299953"
---
# <a name="vml-weight-attribute"></a>Attributo la Weight

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce lo spessore di un tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* weight = " *Expression* " >

**Sintassi dello script**

*element* . Weight = "*Expression*"

*espressione* = *elemento*. peso

**Osservazioni:**

Questo attributo è uguale all'attributo **StrokeWeight** della **forma** e ne esegue l'override. Il valore predefinito è 1 Point.

*Attributo standard la*

**Esempio**

Il tratto ha uno spessore di 5 punti, non 2 punti.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 