---
title: Attributo VML StartArrowWidth
description: Attributo VML StartArrowWidth
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513241"
---
# <a name="vml-startarrowwidth-attribute"></a>Attributo VML StartArrowWidth

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce lo spessore della freccia per l'inizio di una linea. Proprietà di lettura/scrittura. **VgArrowheadWidth**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* startarrowwidth=" *expression* ">

**Sintassi dello script**

*element* .startarrowwidth="*expression*"

*expression* = *elemento*.startarrowwidth

**Osservazioni:**

I possibili valori sono:

-   Stretta
-   Media (impostazione predefinita)
-   Largo

Attributo VML Standard

**Esempio**

Viene disegnata una linea con un'ampia freccia classica all'inizio del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 