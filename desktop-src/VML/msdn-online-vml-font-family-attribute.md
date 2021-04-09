---
title: Attributo Font-Family la
description: Attributo Font-Family la
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047338"
---
# <a name="vml-font-family-attribute"></a>Attributo Font-Family la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la famiglia del tipo di carattere TextPath. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *element* Style = "font-family: *Expression* " >

**Sintassi dello script**

*element* . Style. FontFamily = "*Expression*"

*espressione* = *element*. Style. FontFamily

**Osservazioni:**

Definisce il nome del tipo di carattere. È possibile usare nomi specifici, ad esempio Arial, o tipi generici, ad esempio Serif, sans-serif, corsia, Fantasy o monospace. I valori corrispondono agli attributi di stile HTML standard.

*Attributo standard la*

**Esempio**

La famiglia di caratteri del testo è Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 