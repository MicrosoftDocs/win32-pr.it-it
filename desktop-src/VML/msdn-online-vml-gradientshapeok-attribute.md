---
title: Attributo VML GradientShapeOK
description: Attributo VML GradientShapeOK
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c25620f8ebc05905b83f3abab7b52f7a206b6bafb522b0104f06fd8f46d6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124774"
---
# <a name="vml-gradientshapeok-attribute"></a>Attributo VML GradientShapeOK

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un percorso sfumatura sarà costituito da percorsi incentrati ripetuti. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *elemento* gradientshapeok=" *espressione* ">

**Sintassi dello script**

*element* .gradientshapeok="*expression*"

*expression* = *elemento*.gradientshapeok

**Osservazioni:**

Se **True,** il tracciato verrà riempito con un riempimento sfumato incentrato usando il tracciato come forma ripetuta della sfumatura. Il valore predefinito è **False.**

*Attributo VML Standard*

**Esempio**

Il percorso verrà riempito con un riempimento sfumato incentrato costituito da rettangoli ripetuti.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 