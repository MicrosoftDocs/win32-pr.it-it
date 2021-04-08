---
title: Attributo Origin (Shadow) (la)
description: Attributo Origin (Shadow) (la)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729994"
---
# <a name="origin-attribute-shadowvml"></a>Attributo Origin (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il centro dell'ombreggiatura. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* Origin = " *Expression* " >

**Sintassi dello script**

*element* . Origin = "*Expression*"

*espressione* = *elemento*. Origin

**Osservazioni:**

Coppia di valori frazionari della forma, compresi tra 50% e-50%. Il valore predefinito è 0,0.

*Attributo standard la*

**Esempio**

L'ombreggiatura ha un'origine che è il 20% verso il basso e il 20% a destra dell'origine della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 