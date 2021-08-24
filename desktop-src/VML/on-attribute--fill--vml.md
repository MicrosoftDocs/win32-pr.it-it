---
title: Su attributo (riempimento)(VML)
description: Su attributo (riempimento)(VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee692bf1beb8c9a7c79b50ef8be3c115deea615f18ee6702d0817d4f81439555
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680641"
---
# <a name="on-attribute-fillvml"></a>Su attributo (riempimento)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se il riempimento verrà visualizzato. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* on=" *expression* ">

**Sintassi dello script**

*element* .on="*expression*"

*expression* = *Elemento*.on

**Osservazioni:**

Se **False**, il riempimento non viene visualizzato. Il valore predefinito è **True**.

*Attributo VML Standard*

**Esempio**

Anche se il riempimento è definito rosso, non viene visualizzato.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 