---
title: Attributo Offset2 di la
description: Attributo Offset2 di la
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517050"
---
# <a name="vml-offset2-attribute"></a>Attributo Offset2 di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina un secondo offset. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* offset2 = " *Expression* " >

**Sintassi dello script**

*element* . offset2 = "*Expression*"

*espressione* = *elemento*. offset2

**Osservazioni:**

L'impostazione predefinita per un secondo offset per il valore x è 0 e l'impostazione predefinita per il valore y è 0. I valori sono una misura assoluta o un valore frazionario di forma. Se frazionari, i valori sono compresi tra 50% e-50%.

Usare un secondo offset per creare effetti speciali di ombreggiatura. Per ulteriori informazioni sugli offset secondo, vedere l'attributo [Type](type-attribute--shadow--vml.md) .

*Attributo standard la*

**Esempio**

Viene creata una doppia ombreggiatura per la forma.


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



 

 