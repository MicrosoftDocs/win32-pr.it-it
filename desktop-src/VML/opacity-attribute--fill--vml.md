---
title: Attributo Opacity (Fill) (la)
description: Attributo Opacity (Fill) (la)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730135"
---
# <a name="opacity-attribute-fillvml"></a>Attributo Opacity (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la trasparenza di un riempimento. Proprietà di lettura/scrittura. [VgFraction](msdn-online-vml-vgfraction-data-type.md).

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *elemento* Opacity = " *Expression* " >

**Sintassi dello script**

*element* . Opacity = "*Expression*"

*espressione* = *elemento*. Opacity

**Osservazioni:**

Il valore predefinito è 1,0.

*Attributo standard la*

**Esempio**

Il riempimento della forma sarà trasparente al 50%.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 