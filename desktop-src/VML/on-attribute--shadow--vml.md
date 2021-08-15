---
title: Su attributo (shadow)(VML)
description: Su attributo (shadow)(VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda4d33fbd22d2a7913f13ae8ad874ba3240944f06303f020888aeaafaee88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345852"
---
# <a name="on-attribute-shadowvml"></a>Su attributo (shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se verrà visualizzata un'ombreggiatura. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* on=" *expression* ">

**Sintassi dello script**

*element* .on="*expression*"

*expression* = *Elemento*.on

**Osservazioni:**

Se **True,** verrà visualizzata l'ombreggiatura. Il valore predefinito è **False**.

*Attributo VML Standard*

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





 

 