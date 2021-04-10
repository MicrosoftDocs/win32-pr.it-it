---
title: Attributo offset (Shadow) (la)
description: Attributo offset (Shadow) (la)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963147"
---
# <a name="offset-attribute-shadowvml"></a>Attributo offset (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la distanza con cui l'ombreggiatura si estende oltre la forma. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *elemento* offset = " *Expression* " >

**Sintassi dello script**

*element* . offset = "*Expression*"

*espressione* = *elemento*. offset

**Osservazioni:**

L'offset predefinito per il valore x è 2PT e l'impostazione predefinita per il valore y è 2Pt. I valori sono una misura assoluta o un valore frazionario di forma. Se frazionarie, variano da 50% a-50%.

*Attributo standard la*

**Esempio**

La forma presenta un'ombreggiatura con un offset di 5 punti verso il basso e 10 punta a destra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 