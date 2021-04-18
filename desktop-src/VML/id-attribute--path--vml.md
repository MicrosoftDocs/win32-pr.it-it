---
title: Attributo ID (percorso) (la)
description: Attributo ID (percorso) (la)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117775"
---
# <a name="id-attribute-pathvml"></a>Attributo ID (percorso) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Nome che fornisce un identificatore univoco per un percorso. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* ID = " *Expression* " >

**Sintassi dello script**

*element* . ID = "*Expression*"

*espressione* = *elemento*. ID

**Osservazioni:**

Usare **ID** per fare riferimento a un percorso specifico. Una volta creato un percorso e dato un ID, è possibile utilizzare il nome dell'ID quando si desidera modificare il percorso.

*Attributo standard la*

**Esempio**

La forma ha un ID di percorso denominato "percorso".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 