---
title: Attributo color2 (Fill) (la)
description: Attributo color2 (Fill) (la)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300222"
---
# <a name="color2-attribute-fillvml"></a>Attributo color2 (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un secondo colore per le compilazioni. Proprietà di lettura/scrittura. [VgColor](msdn-online-vml-ivgcolor.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* color2 = " *Expression* " >

**Sintassi dello script**

*element* . color2 = "*Expression*"

*espressione* = *elemento*. color2

**Osservazioni:**

Viene usato un secondo colore quando un tipo di riempimento è un modello o una sfumatura. Il valore predefinito è **bianco**.

*Attributo standard la*

**Esempio**

Il tipo di riempimento della forma è un modello in cui il riempimento in primo piano viene definito dall'immagine di origine, ma lo sfondo trasparente viene definito dal secondo colore.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 