---
title: Attributo ImageSize di VML
description: Attributo ImageSize di VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be63fb0adf39e2494ae2fa4d1037b96c7873a7c12524215de0d1ecfd016e116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600247"
---
# <a name="vml-imagesize-attribute"></a>Attributo ImageSize di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce le dimensioni dell'immagine per il tratto. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* imagesize=" *expression* ">

**Sintassi dello script**

*element* .imagesize="*expression*"

*expression* = *elemento*.imagesize

**Osservazioni:**

Il valore predefinito è la dimensione dell'immagine.

*Attributo standard VML*

**Esempio**

L'immagine del tratto avrà dimensioni di 10 per 10 punti.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 