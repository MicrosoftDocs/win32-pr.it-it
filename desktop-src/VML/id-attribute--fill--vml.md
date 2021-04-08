---
title: Attributo ID (Fill) (la)
description: Attributo ID (Fill) (la)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047018"
---
# <a name="id-attribute-fillvml"></a>Attributo ID (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Nome che fornisce un identificatore univoco per un riempimento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* ID = " *Expression* " >

**Sintassi dello script**

*element* . ID = "*Expression*"

*espressione* = *elemento*. ID

**Osservazioni:**

Usare **ID** per fare riferimento a un riempimento specifico. Una volta creato un riempimento e fornito un ID, è possibile utilizzare il nome ID quando si desidera modificare il riempimento.

*Attributo standard la*

**Esempio**

La forma dispone di un ID di riempimento denominato "riempimento".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 