---
title: Attributo la V
description: Attributo la V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117942"
---
# <a name="vml-v-attribute"></a>Attributo la V

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce i comandi che costituiscono un percorso. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* v = " *Expression* " >

**Sintassi dello script**

*element* . v = "*Expression*"

*espressione* = *elemento*. v

**Osservazioni:**

Esegue l'override dell'attributo **path** di una forma. Le coordinate possono essere numeri fissi, numeri relativi o riferimenti alle formule (usando il formato " @n ", dove n è un numero di formula. ad esempio, " @2 " si riferisce alla seconda formula nella matrice di formule).

*Attributo standard la*

**Esempio**

Un rettangolo viene creato usando l'attributo **V** . Si noti che viene usata una lettera minuscola L (comando **LineTo** ) dopo il primo set di coordinate delimitate da virgole.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 