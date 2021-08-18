---
title: Attributo VML EndArrow
description: Attributo VML EndArrow
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f289342c8bfb67e9a0c2ccc6e418f42bd954e9826a18f07260a2891bf4b4284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007831"
---
# <a name="vml-endarrow-attribute"></a>Attributo VML EndArrow

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce una freccia per la fine di una linea. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* endarrow=" *expression* ">

**Sintassi dello script**

*element* .endarrow="*expression*"

*expression* = *elemento*.endarrow

**Osservazioni:**

I possibili valori sono:

-   Nessuno (valore predefinito)
-   Blocca
-   Classic
-   Diamond
-   Ovale
-   Apri

*Attributo VML Standard*

**Esempio**

Viene disegnata una linea con una freccia classica alla fine del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 