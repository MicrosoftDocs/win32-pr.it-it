---
title: Attributo VML Aspect
description: Attributo VML Aspect
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669b0f93e740e6bc4d4fb94155f6ca0ab60d5e00cebfb1604d5272d45d4dd8ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602898"
---
# <a name="vml-aspect-attribute"></a>Attributo VML Aspect

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica come verranno mantenute le proporzioni dell'immagine di riempimento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* aspect=" *expression* ">

**Sintassi dello script**

*element* .aspect="*expression*"

*expression* = *elemento*.aspect

**Osservazioni:**

I possibili valori sono:



| Valore   | Descrizione                           |
|---------|---------------------------------------|
| ignore  | Ignorare i problemi relativi all'aspetto. Valore predefinito.        |
| Atleast | Le dimensioni dell'immagine sono almeno di **dimensioni .** |
| a rieti  | L'immagine non è più grande di **Dimensioni**.     |



 

*Attributo VML Standard*

**Esempio**

L'immagine che costituisce il riempimento è maggiore o uguale a una dimensione di 10 punti per 10 punti.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 