---
title: Attributo VML V-Text-Reverse
description: Attributo VML V-Text-Reverse
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f1535620c1fefe98ac23e2f842ef9a97e13b9cb39c65ec6b97f6f7d12b1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654621"
---
# <a name="vml-v-text-reverse-attribute"></a>Attributo VML V-Text-Reverse

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se l'ordine di layout delle righe è invertito. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="v-text-reverse: *expression* ">

**Sintassi dello script**

*element* .style.v-text-reverse="*expression*"

*expression* = *elemento*.style.v-text-reverse

**Osservazioni:**

Se **True**, l'ordine di layout delle righe viene invertito. Questo attributo viene usato per il layout verticale del testo. Il valore predefinito è **False**.

*Attributo VML Standard*

**Esempio**

L'ordine del layout è invertito.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 