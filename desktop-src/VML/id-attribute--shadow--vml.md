---
title: Attributo ID (Shadow) (la)
description: Attributo ID (Shadow) (la)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728343"
---
# <a name="id-attribute-shadowvml"></a>Attributo ID (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica un nome che fornisce un identificatore univoco per un'ombreggiatura. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* ID = " *Expression* " >

**Sintassi dello script**

*element* . ID = "*Expression*"

*espressione* = *elemento*. ID

**Osservazioni:**

Usare **ID** per fare riferimento a un'ombreggiatura specifica. Dopo aver creato un'ombreggiatura e dato un ID, è possibile usare il nome ID quando si desidera modificare l'ombreggiatura.

*Attributo standard la*

**Esempio**

Alla forma è associato un ID ombreggiatura denominato "ombreggiatura".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 