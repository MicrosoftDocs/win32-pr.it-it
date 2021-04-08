---
title: Attributo Font-Style la
description: Attributo Font-Style la
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046818"
---
# <a name="vml-font-style-attribute"></a>Attributo Font-Style la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la quantità di inclinazione per un tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "font-style: *Expression* " >

**Sintassi dello script**

*element* . Style. FontStyle = "*Expression*"

*espressione* = *element*. Style. FontStyle

**Osservazioni:**

I valori possibili sono:

-   normale (impostazione predefinita)
-   obliquo
-   Corsivo

Molti browser eseguono il rendering obliquo come corsivo. I valori corrispondono agli attributi di stile HTML standard.

*Attributo standard la*

**Esempio**

Il tipo di carattere è corsivo (inclinato).


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 