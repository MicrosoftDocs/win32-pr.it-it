---
title: Attributo VML Offset2
description: Attributo VML Offset2
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc06b68f075b139f6822a38672b8530fc2172071aab35072659968725d9866b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124224"
---
# <a name="vml-offset2-attribute"></a>Attributo VML Offset2

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina un secondo offset. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* offset2=" *expression* ">

**Sintassi dello script**

*element* .offset2="*expression*"

*expression* = *elemento*.offset2

**Osservazioni:**

Il valore predefinito per un secondo offset per il valore x è 0 e il valore predefinito per il valore y è 0. I valori sono una misura assoluta o un valore frazionario di forma. Se frazionari, i valori sono compreso tra 50% e -50%.

Usare un secondo offset per creare effetti ombreggiati speciali. Per altre [informazioni sui](type-attribute--shadow--vml.md) secondi offset, vedere l'attributo Type.

*Attributo VML Standard*

**Esempio**

Per la forma viene creata un'ombreggiatura doppia.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 