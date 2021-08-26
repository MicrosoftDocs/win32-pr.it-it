---
title: Attributo di taglio VML
description: Attributo di taglio VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05f7463465c10abb4f4f01267a7ebeac878cbf36c41f1effde6ec218bad1088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974612"
---
# <a name="vml-trim-attribute"></a>Attributo di taglio VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se lo spazio aggiuntivo viene rimosso sopra e sotto il testo. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="trim: *expression* ">

**Sintassi dello script**

*element* .style.trim="*expression*"

*expression* = *elemento*.style.trim

**Osservazioni:**

Se **True,** lo spazio riservato agli ascendenti e ai discendenti viene rimosso. Il valore predefinito è **False**.

*Attributo standard VML*

**Esempio**

Lo spazio aggiuntivo sopra e sotto viene tagliato.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 