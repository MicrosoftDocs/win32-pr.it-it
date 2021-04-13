---
title: Attributo Opacity (Shadow) (la)
description: Attributo Opacity (Shadow) (la)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399157"
---
# <a name="opacity-attribute-shadowvml"></a>Attributo Opacity (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina la trasparenza di un'ombreggiatura. Proprietà di lettura/scrittura. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *elemento* Opacity = " *Expression* " >

**Sintassi dello script**

*element* . Opacity = "*Expression*"

*espressione* = *elemento*. Opacity

**Osservazioni:**

Il valore predefinito è 1. Il valore 0 renderà un'ombreggiatura completamente trasparente.

*Attributo standard la*

**Esempio**

La forma presenta un'ombreggiatura trasparente al 50%.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 