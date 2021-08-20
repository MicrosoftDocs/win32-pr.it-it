---
title: Attributo Color2 (Stroke)(VML)
description: Attributo Color2 (Stroke)(VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108c767f7337f486f8b7df5a4506b3b3d487dabf146656890def0c5e1ad32a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867431"
---
# <a name="color2-attribute-strokevml"></a>Attributo Color2 (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un secondo colore per i tratti. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* color2=" *expression* ">

Sintassi dello script

*element* .color2="*expression*"

*expression* = *elemento*.color2

**Osservazioni:**

Un secondo colore viene usato quando il tipo di riempimento di un tratto è un motivo.

*Attributo VML Standard*

**Esempio**

Il tratto della forma è un riempimento a motivo in cui il riempimento è definito dall'immagine di origine, ma lo sfondo trasparente è definito dal secondo colore.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 