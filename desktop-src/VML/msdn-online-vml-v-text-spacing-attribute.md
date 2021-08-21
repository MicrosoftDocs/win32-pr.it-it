---
title: Attributo VML V-Text-Spacing
description: Attributo VML V-Text-Spacing
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0b699e70cd235bf7d0f7530f75a8fc5eaef52974180cc8d36a10a69c9197f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057679"
---
# <a name="vml-v-text-spacing-attribute"></a>Attributo VML V-Text-Spacing

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la quantità di spaziatura per il testo. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="v-text-spacing: *expression* ">

**Sintassi dello script**

*element* .style.v-text-spacing="*expression*"

*expression* = *elemento*.style.v-text-spacing

**Osservazioni:**

Il valore predefinito è 100. Per altre informazioni sulla spaziatura del testo, vedere l'attributo [V-Text-Spacing-Mode.](msdn-online-vml-v-text-spacing-mode-attribute.md)

*Attributo VML Standard*

**Esempio**

La combinazione di lettere tra ogni lettera viene restringeta di 200 unità.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 