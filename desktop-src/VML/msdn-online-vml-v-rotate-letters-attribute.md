---
title: Attributo VML V-Rotate-Letters
description: Attributo VML V-Rotate-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779f7878b01765416560dacaed5e3b81a1e00a25d4bf7c53e0071c8bb487d16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123781"
---
# <a name="vml-v-rotate-letters-attribute"></a>Attributo VML V-Rotate-Letters

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se le lettere del testo vengono ruotate. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="v-rotate-letters: *expression* ">

**Sintassi dello script**

*element* .style.v-rotate-letters="*expression*"

*expression* = *element*.style.v-rotate-letters

**Osservazioni:**

Se **True,** le lettere del testo vengono ruotate di 90 gradi. Il valore predefinito è **False**.

*Attributo VML Standard*

**Esempio**

Le lettere vengono ruotate di 90 gradi.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 