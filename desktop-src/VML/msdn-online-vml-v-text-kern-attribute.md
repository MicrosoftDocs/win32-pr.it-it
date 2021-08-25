---
title: Attributo VML V-Text-Kern
description: Attributo VML V-Text-Kern
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5ca41b66c05af673839ccbc8ba9eb95cf652eb223cd4dd3915799e91ff6c69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974631"
---
# <a name="vml-v-text-kern-attribute"></a>Attributo VML V-Text-Kern

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se la crenatura è attivata. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="v-text-kern: *expression* ">

**Sintassi dello script**

*element* .style.v-text-kern="*expression*"

*expression* = *elemento*.style.v-text-kern

**Osservazioni:**

Se **True,** la crenatura è attivata. Il valore predefinito è **False**. La crenatura è la rimozione di spazio tra determinate coppie di lettere per compensare forme di lettera non uniforme. Ad esempio, se la crenatura è attivata, verrà rimosso lo spazio aggiuntivo tra una "T" maiuscola e una "i" minuscola.

*Attributo VML Standard*

**Esempio**

La crenatura è attivata.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 