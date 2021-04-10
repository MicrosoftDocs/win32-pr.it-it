---
title: Attributo on (Shadow) (la)
description: Attributo on (Shadow) (la)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963291"
---
# <a name="on-attribute-shadowvml"></a>Attributo on (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se verrà visualizzata un'ombreggiatura. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* on = " *Expression* " >

**Sintassi dello script**

*element* . on = "*Expression*"

*espressione* = *elemento*. on

**Osservazioni:**

Se **true**, verrà visualizzata l'ombreggiatura. Il valore predefinito è **False**.

*Attributo standard la*

**Esempio**

Verrà visualizzata l'ombreggiatura.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 