---
title: Attributo StartArrowLength di la
description: Attributo StartArrowLength di la
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399294"
---
# <a name="vml-startarrowlength-attribute"></a>Attributo StartArrowLength di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la lunghezza della freccia per l'inizio di una riga. Proprietà di lettura/scrittura. **VgArrowheadLength**.

**Si applica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintassi Tag**

<v: *element* startarrowlength = " *Expression* " >

**Sintassi dello script**

*element* . startarrowlength = "*Expression*"

*espressione* = *elemento*. startarrowlength

**Osservazioni:**

I possibili valori sono:

-   Short
-   Media (impostazione predefinita)
-   long

Attributo standard la

**Esempio**

Viene disegnata una linea con una breve freccia classica all'inizio del tratto.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 