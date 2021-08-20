---
title: Attributo master VML
description: Attributo master VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d126b9d02144bbc8831d7be9e73a3e5896c2ceccca71cfcbc8161d5ccc8112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999111"
---
# <a name="vml-master-attribute"></a>Attributo master VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un **elemento ShapeType** è un elemento master. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[ShapeType](msdn-online-vml-shapetype-element.md)

**Sintassi dei tag**

<v: *element* o:master=" *expression* ">

**Osservazioni:**

Se **True,** il **rendering della forma ShapeType** viene eseguito dal motore di rendering. Il valore predefinito è **False**.

*Microsoft Office Attributo Extensions*

**Esempio**

**L'elemento ShapeType** è una forma master.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 