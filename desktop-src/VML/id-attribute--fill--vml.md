---
title: Attributo ID (fill)(VML)
description: Attributo ID (fill)(VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f317cef4d588444f5c01770dafd5b56af0d2bca48ee228ff789a11b46348bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007871"
---
# <a name="id-attribute-fillvml"></a>Attributo ID (fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Nome che fornisce un identificatore univoco per un riempimento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* id=" *expression* ">

**Sintassi dello script**

*element* .id="*expression*"

*expression* = *elemento*.id

**Osservazioni:**

Usare **l'ID** per fare riferimento a un riempimento specifico. Dopo aver creato un riempimento e aver assegnato un ID, è possibile usare il nome ID quando si vuole modificare il riempimento.

*Attributo standard VML*

**Esempio**

La forma ha un ID riempimento denominato "myfill".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 