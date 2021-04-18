---
title: Attributo font la
description: Attributo font la
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300398"
---
# <a name="vml-font-attribute"></a>Attributo font la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica un valore composto di attributi del tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "font: *Expression* " >

**Sintassi dello script**

*element* . Style. font = "*Expression*"

*espressione* = *element*. Style. font

**Osservazioni:**

Definisce gli attributi di un tipo di carattere, inclusi famiglia, stile, peso, dimensioni e Variant. L'ordine delle definizioni nella stringa è: tipo di **carattere**, **variante del tipo** di carattere, **spessore** del carattere, dimensioni del **carattere**, **altezza della riga** e **famiglia di caratteri**. I valori corrispondono agli attributi di stile HTML standard.

*Attributo standard la*

**Esempio**

Il tipo di carattere del testo TextPath è Italic, Small Caps, Bold, 36 Point Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 