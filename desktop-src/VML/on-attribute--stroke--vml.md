---
title: On Attribute (Stroke)(VML)
description: On Attribute (Stroke)(VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5682200a44a98d2b4c074b11db172e2b94b812a196a404927a33b4d142289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007571"
---
# <a name="on-attribute-strokevml"></a>On Attribute (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se il tratto verrà visualizzato. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* on=" *expression* ">

**Sintassi dello script**

*element* .on="*expression*"

*expression* = *Elemento*.on

**Osservazioni:**

Se **False**, il tratto non viene visualizzato. Il valore predefinito è **True**.

*Attributo VML Standard*

**Esempio**

Il tratto non verrà visualizzato.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 