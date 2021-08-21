---
title: Attributo VML MSO-Wrap-Distance-Right
description: Attributo VML MSO-Wrap-Distance-Right
ms.assetid: 2f0ec7a3-036e-4f45-a330-f8ddccb75791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7984c44325e62f3192725a52f2730b3ebcfc1daa78524855f8416fb840472d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124321"
---
# <a name="vml-mso-wrap-distance-right-attribute"></a>Attributo VML MSO-Wrap-Distance-Right

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la distanza dal lato destro della forma al testo che la racchiude. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="mso-wrap-distance-right: *expression* ">

**Osservazioni:**

Si noti che questo attributo è diverso dall'attributo CSS **Margin.** **Margin** modifica l'origine della forma per includere le aree dei margini, ma la distanza di ritorno a capo Microsoft Office non modifica l'origine della forma.

*Microsoft Office Attributo Extensions*

**Esempio**

La forma ha una distanza di ritorno a capo a destra di 10 punti.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-right:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 