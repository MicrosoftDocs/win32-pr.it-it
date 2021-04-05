---
title: Attributo EndArrowWidth di la
description: Attributo EndArrowWidth di la
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730154"
---
# <a name="vml-endarrowwidth-attribute"></a>Attributo EndArrowWidth di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la larghezza della freccia per la fine di una riga. Proprietà di lettura/scrittura. **VgArrowheadWidth**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* endarrowwidth = " *Expression* " >

**Sintassi dello script**

*element* . endarrowwidth = "*Expression*"

*espressione* = *elemento*. endarrowwidth

**Osservazioni:**

I possibili valori sono:

-   Limitare
-   Media (impostazione predefinita)
-   Largo

*Attributo standard la*

**Esempio**

Una linea viene disegnata con una freccia classica ampia alla fine del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 