---
title: LA clip-attributo
description: LA clip-attributo
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300018"
---
# <a name="vml-clip-attribute"></a>LA clip-attributo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se il ritaglio è on. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi Tag**

<v: *elemento* clip = " *Expression* " >

**Sintassi dello script**

*element* . clip = "*Expression*"

*espressione* = *elemento*. clip

**Osservazioni:**

Se il **clip** è **false**, la forma verrà ridimensionata in base al frame. Se **true**, tutte le parti della forma che si trovano all'esterno del frame non verranno visualizzate.

Si noti che l' [origine](origin-attribute--vmlframe--vml.md) e le [dimensioni](size-attribute--vmlframe.md) non verranno utilizzate a meno che la **clip** non sia **true**.

*Attributo standard la*

**Esempio**

L'immagine definita nel file esterno verrà ritagliata.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 