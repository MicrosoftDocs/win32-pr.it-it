---
title: La MSO-wrap-distance-Top attributo
description: La MSO-wrap-distance-Top attributo
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a16898733ead7bf3728d8f520888c8a05ef5fe6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300006"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a>La MSO-wrap-distance-Top attributo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la distanza tra l'inizio della forma e il testo che lo racchiude. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* Style = "MSO-wrap-distance-Top: *Expression* " >

**Osservazioni:**

Si noti che questo attributo è diverso dall'attributo del **margine** CSS. **Margin** modifica l'origine della forma in modo da includere le aree dei margini, ma la distanza dal ritorno a capo nell'Microsoft Office non modifica l'origine della forma.

*Attributo Microsoft Office Extensions*

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



 

 