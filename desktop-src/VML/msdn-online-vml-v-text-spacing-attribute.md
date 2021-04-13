---
title: Attributo la V-text-spaziatura
description: Attributo la V-text-spaziatura
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399375"
---
# <a name="vml-v-text-spacing-attribute"></a>Attributo la V-text-spaziatura

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la quantità di spaziatura per il testo. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *elemento* Style = "v-text-spaziation: *Expression* " >

**Sintassi dello script**

*element* . Style. v-text-spaziation = "*Expression*"

*espressione* = *elemento*. Style. v-spaziatura testo

**Osservazioni:**

Il valore predefinito è 100. Per ulteriori informazioni sulla spaziatura del testo, vedere l'attributo [V-text-spaziation-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .

*Attributo standard la*

**Esempio**

Il letterSpacing tra ogni lettera viene ristretto di 200 unità.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 