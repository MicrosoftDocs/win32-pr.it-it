---
title: Attributo vml Font-Style
description: Attributo vml Font-Style
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4571f9805b3a12f1c3c7b340780d0f3d9f6ce8644c2ec501e8c93aa58d378de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057859"
---
# <a name="vml-font-style-attribute"></a>Attributo vml Font-Style

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la quantità di inclinazione per un tipo di carattere. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso di testo](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* style="font-style: *expression* ">

**Sintassi dello script**

*element* .style.fontstyle="*expression*"

*expression* = *elemento*.style.fontstyle

**Osservazioni:**

I valori possibili sono:

-   normal (impostazione predefinita)
-   Obliquo
-   Corsivo

La maggior parte dei browser esegue il rendering obliqua in corsivo. I valori sono gli stessi degli attributi di stile HTML standard.

*Attributo VML Standard*

**Esempio**

Il tipo di carattere è in corsivo (s inclinazione).


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 