---
title: LA-attributo oscurato
description: LA-attributo oscurato
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046948"
---
# <a name="vml-obscured-attribute"></a>LA-attributo oscurato

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un'ombreggiatura è trasparente. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* Obscured = " *Expression* " >

**Sintassi dello script**

*element* . Obscured = "*Expression*"

*espressione* = *elemento*. Obscured

**Osservazioni:**

Se **true**, consente di visualizzare l'ombreggiatura se non è presente alcun riempimento della forma. L'impostazione predefinita è **False**.

*Attributo standard la*

**Esempio**

Lo sfondo viene visualizzato attraverso l'ombreggiatura.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 