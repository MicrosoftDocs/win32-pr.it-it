---
title: Attributo origin (Shadow)(VML)
description: Attributo origin (Shadow)(VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1776b0d8a857a3247543eae13d280d023585229d27c04a576420003ea53920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959181"
---
# <a name="origin-attribute-shadowvml"></a>Attributo origin (Shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il centro dell'ombreggiatura. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* origin=" *expression* ">

**Sintassi dello script**

*element* .origin="*expression*"

*expression* = *elemento*.origin

**Osservazioni:**

Coppia di valori frazionari della forma, compresi tra il 50% e il -50%. Il valore predefinito è 0,0.

*Attributo VML Standard*

**Esempio**

L'ombreggiatura ha un'origine inferiore del 20% e del 20% a destra dell'origine della forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 