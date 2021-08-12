---
title: Attributo offset (Shadow)(VML)
description: Attributo offset (Shadow)(VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0683e9536e10bed141ecca56b4335d6221c5ced7e3d26220908aa388b453843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596906"
---
# <a name="offset-attribute-shadowvml"></a>Attributo offset (Shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'estensione dell'ombreggiatura oltre la forma. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* offset=" *expression* ">

**Sintassi dello script**

*element* .offset="*expression*"

*expression* = *elemento*.offset

**Osservazioni:**

L'offset predefinito per il valore x è 2pt e il valore predefinito per il valore y è 2pt. I valori sono una misura assoluta o un valore frazionario di forma. Se frazionarie, vanno dal 50% al -50%.

*Attributo standard VML*

**Esempio**

La forma ha un'ombreggiatura con un offset di 5 punti verso il basso e 10 punti a destra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 