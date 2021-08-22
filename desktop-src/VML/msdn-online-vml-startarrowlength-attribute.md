---
title: Attributo VML StartArrowLength
description: Attributo VML StartArrowLength
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25446737118c546727d769d54d98e4503faaadd063102fa98a417ebea13c976d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395831"
---
# <a name="vml-startarrowlength-attribute"></a>Attributo VML StartArrowLength

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la lunghezza della freccia per l'inizio di una linea. Proprietà di lettura/scrittura. **VgArrowheadLength**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* startarrowlength=" *expression* ">

**Sintassi dello script**

*element* .startarrowlength="*expression*"

*expression* = *elemento*.startarrowlength

**Osservazioni:**

I possibili valori sono:

-   Short
-   Media (impostazione predefinita)
-   long

Attributo standard VML

**Esempio**

Viene disegnata una linea con una breve freccia classica all'inizio del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 