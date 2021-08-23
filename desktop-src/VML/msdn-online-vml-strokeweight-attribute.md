---
title: Attributo StrokeWeight VML
description: Attributo StrokeWeight VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac5efa964607fdd942c8dff31a4a124d424aa5fbfeede27abc6164fddef087
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680681"
---
# <a name="vml-strokeweight-attribute"></a>Attributo StrokeWeight VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce lo spessore del pennello che traccia il percorso di una forma. Proprietà di lettura/scrittura. **VGLength**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* strokeweight=" *espressione* ">

**Sintassi dello script**

*element* .strokeweight="*expression*"

*expression* = *elemento*.strokeweight

**Osservazioni:**

Il valore viene duplicato **dall'attributo Weight** dell'elemento **Stroke.** Se viene specificato un numero, ma non viene aggiunta alcuna unità, l'unità di misura predefinita è emu. Se non viene specificato alcun valore, il valore predefinito è 1 pixel (1px).

Per gli script, tuttavia, l'unità di misura predefinita è in punti.

*Attributo standard VML*

**Vedere anche**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)

**Esempio**

Lo spessore del tratto della forma è di 1 punto.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo StrokeWeight](/previous-versions/bb264095(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 