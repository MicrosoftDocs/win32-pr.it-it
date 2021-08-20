---
title: Attributo Color (Fill)(VML)
description: Attributo Color (Fill)(VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ec72cab0562ae675ca2e22992369a7c0ad6534207cd2a6f6141f56c64e2f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125381"
---
# <a name="color-attribute-fillvml"></a>Attributo Color (Fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il colore di un riempimento. Proprietà di lettura/scrittura. **VgColor**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* color=" *expression* ">

**Sintassi dello script**

*element* .color="*expression*"

*expression* = *elemento*.color

**Osservazioni:**

Esegue l'override **dell'attributo FillColor** di una forma. Il valore predefinito è **White.**

*Attributo VML Standard*

**Esempio**

Il colore di riempimento della forma è verde.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 