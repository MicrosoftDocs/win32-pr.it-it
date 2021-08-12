---
title: Attributo LineStyle VML
description: Attributo LineStyle VML
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90be9c2aceeb3663f55c92e1140eb6a12f66aa23dd8856d0da63f0a306d8cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598284"
---
# <a name="vml-linestyle-attribute"></a>Attributo LineStyle VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce lo stile della linea del tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *elemento* linestyle=" *espressione* ">

**Sintassi dello script**

*element* .linestyle="*expression*"

*expression* = *elemento*.linestyle

**Osservazioni:**

I possibili valori sono:

-   Single (impostazione predefinita)
-   ThinThin
-   ThinThick
-   ThickThin
-   ThickBetweenThin

*Attributo standard VML*

**Esempio**

Viene disegnata una linea doppia con due tratti sottili.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 