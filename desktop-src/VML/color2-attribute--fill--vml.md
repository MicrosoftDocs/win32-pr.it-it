---
title: Attributo Color2 (Riempimento)(VML)
description: Attributo Color2 (Riempimento)(VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e651245ddf9fb2a3669c3529038b5d0d8cbb3922b8a112c201858d2efd786a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007891"
---
# <a name="color2-attribute-fillvml"></a>Attributo Color2 (Riempimento)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un secondo colore per i riempimenti. Proprietà di lettura/scrittura. [VgColor](msdn-online-vml-ivgcolor.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* color2=" *expression* ">

**Sintassi dello script**

*element* .color2="*expression*"

*expression* = *elemento*.color2

**Osservazioni:**

Un secondo colore viene usato quando un tipo di riempimento è un motivo o una sfumatura. Il valore predefinito è **White.**

*Attributo standard VML*

**Esempio**

Il tipo di riempimento della forma è un motivo in cui il riempimento in primo piano è definito dall'immagine di origine, ma lo sfondo trasparente è definito dal secondo colore.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 