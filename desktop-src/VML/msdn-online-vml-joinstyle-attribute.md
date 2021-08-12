---
title: Attributo VML JoinStyle
description: Attributo VML JoinStyle
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbad649d2a8889846d1d0c1e1df3d62e94cb8e8ff03f0dfa5c47f7bd414dcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599365"
---
# <a name="vml-joinstyle-attribute"></a>Attributo VML JoinStyle

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce lo stile di join di una polilinea. Proprietà di lettura/scrittura. Stringa.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* joinstyle=" *expression* ">

**Sintassi dello script**

*element* .joinstyle="*expression*"

*expression* = *elemento*.joinstyle

**Osservazioni:**

I possibili valori sono:

-   round (impostazione predefinita)
-   smussatura
-   Miter

*Attributo VML Standard*

**Esempio**

Le giunzioni sulla polilinea vengono smussate.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 