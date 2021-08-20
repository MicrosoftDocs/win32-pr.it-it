---
title: Attributo VML MSO-Wrap-Distance-Top
description: Attributo VML MSO-Wrap-Distance-Top
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856082665ab1b46b9d9294bffdd2821e2fb5db4b6e066effef5dd2f081185f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124291"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a>Attributo VML MSO-Wrap-Distance-Top

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce la distanza dalla parte superiore della forma al testo che la racchiude. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="mso-wrap-distance-top: *expression* ">

**Osservazioni:**

Si noti che questo attributo è diverso dall'attributo **CSS Margin.** **Il** margine modifica l'origine della forma in modo da includere le aree del margine, ma la distanza di ritorno a capo Microsoft Office modifica l'origine della forma.

*Microsoft Office Attributo Extensions*

**Esempio**

La forma ha una distanza di ritorno a capo superiore di 10 punti.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 