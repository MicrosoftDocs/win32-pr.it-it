---
title: Attributo origin (fill)(VML)
description: Attributo origin (fill)(VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc33ae1f4cf7c588ae9b3f40ff8c445be88192bae1dfc86a3593eea931befb25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959221"
---
# <a name="origin-attribute-fillvml"></a>Attributo origin (fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il centro di un'immagine di riempimento. Proprietà di lettura/scrittura. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* origin=" *expression* ">

**Sintassi dello script**

*element* .origin="*expression*"

*expression* = *elemento*.origin

**Osservazioni:**

Specifica un punto relativo all'angolo superiore sinistro dell'immagine. questo punto viene considerato come l'origine dell'immagine. Il valore predefinito è il centro dell'immagine. Il vettore è una frazione della larghezza e dell'altezza dell'immagine.

*Attributo standard VML*

**Esempio**

L'immagine del riempimento viene spostata a sinistra fino a un punto del 50% della larghezza della forma .


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 