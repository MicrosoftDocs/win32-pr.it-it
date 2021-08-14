---
title: Attributo compilato VML
description: Attributo compilato VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7053263f989dbbef163e04ca19e28afa882d20347b103c97cf2db3be4b8d25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346605"
---
# <a name="vml-filled-attribute"></a>Attributo compilato VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se il percorso chiuso verrà riempito. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* filled=" *expression* ">

**Sintassi dello script**

*element* .filled="*expression*"

*expression* = *elemento*.filled

**Osservazioni:**

Il valore viene duplicato **dall'attributo On** dell'elemento [Fill.](msdn-online-vml-fill-element.md)

*Attributo VML Standard*

**Esempio**

Il tracciato della forma è riempito.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo compilato](/previous-versions/bb229669(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 