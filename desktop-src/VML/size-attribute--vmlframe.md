---
title: Attributo size (VMLFrame)
description: Attributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046808"
---
# <a name="size-attribute-vmlframe"></a>Attributo size (VMLFrame)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce le dimensioni dell'area di visualizzazione del frame. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi Tag**

<v: *element* size = " *Expression* " >

**Sintassi dello script**

*element* . size = "*Expression*"

*espressione* = *element*. size

**Osservazioni:**

Il valore predefinito è 0,0. Si noti che la **dimensione** funziona solo se il [clip](msdn-online-vml-clip-attribute.md) è **true**. In questo attributo, le dimensioni sono definite come larghezza e altezza del frame.

*Attributo standard la*

**Esempio**

Le dimensioni dell'area di ridimensionamento saranno 50pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 