---
title: Attributo VML Chromakey
description: Attributo VML Chromakey
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d279f31ff4910ceb121242f587aac88585dba2cfc8278320c0d86680f4f330b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999311"
---
# <a name="vml-chromakey-attribute"></a>Attributo VML Chromakey

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il valore del colore dell'immagine che verrà considerata trasparente. Proprietà di lettura/scrittura. **VgColor**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* chromakey=" *expression* ">

**Sintassi dello script**

*element* .chromakey="*expression*"

*expression* = *elemento*.chromakey

**Osservazioni:**

Usare questo attributo per rendere trasparenti parti di un'immagine impostando la trasparenza su un colore specifico. Ad esempio, se si imposta il valore **Chromakey** su **nero,** qualsiasi parte dell'immagine nera sarà trasparente e il colore di riempimento "verrà visualizzato attraverso" tale parte dell'immagine.

*Attributo VML Standard*

**Esempio**

Le aree dell'immagine a tinta unita nere diventeranno trasparenti, consentendo al colore di riempimento verde di passare attraverso tali aree.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 