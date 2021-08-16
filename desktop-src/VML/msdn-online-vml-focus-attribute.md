---
title: Attributo vml focus
description: Attributo vml focus
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60eeb9ff379c8006cbb9068b6b78c8f24490ecf2fd15573b5b224a9ee1208ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057869"
---
# <a name="vml-focus-attribute"></a>Attributo vml focus

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il centro di un riempimento sfumato lineare. Proprietà di lettura/scrittura. **VgFraction**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *elemento* focus=" *espressione* ">

**Sintassi dello script**

*element* .focus="*expression*"

*expression* = *elemento*.focus

**Osservazioni:**

Definisce la posizione iniziale centrale della fusione. I valori sono compreso tra 100% e -100%. Il valore predefinito è 0. Un valore pari a 100% (o -100%) sposta lo stato attivo in modo che la direzione della fusione si inverti (invertendo di fatto **Color** **e Color2).** Il valore 50% modificherà la fusione in modo che **Color** sia a entrambe le estremità e **Color2** sia al centro. Il valore -50% modificherà la fusione in modo che **Color2** sia a entrambe le estremità e **Color** sia al centro.

*Attributo VML Standard*

**Esempio**

Lo stato attivo della sfumatura del riempimento viene spostato in modo che il rosso (**Color**) sia una banda al centro della forma e che la parte superiore e inferiore siano blu (**Color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 