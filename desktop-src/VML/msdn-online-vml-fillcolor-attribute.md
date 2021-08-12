---
title: Attributo VML FillColor
description: Attributo VML FillColor
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e626e017437d14cf1088c188e659e1099dc38c7ba88215438a6c9a45166c7732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601361"
---
# <a name="vml-fillcolor-attribute"></a>Attributo VML FillColor

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il colore del pennello che riempie il tracciato chiuso di una forma. Proprietà di lettura/scrittura. [Oggetto IVgColor.](msdn-online-vml-ivgcolor.md)

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* fillcolor=" *expression* ">

**Sintassi dello script**

*element* .fillcolor="*expression*"

*expression* = *elemento*.fillcolor

**Osservazioni:**

Il **valore FillColor** viene duplicato dall'attributo **Color** dell'elemento **Fill.**

*Attributo VML Standard*

**Vedere anche**

[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)

**Esempio**

Il colore di riempimento del rettangolo è rosso.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo FillColor](/previous-versions/bb229668(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 