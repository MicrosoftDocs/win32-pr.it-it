---
title: Attributo VML MiterLimit
description: Attributo VML MiterLimit
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef82ce7e8e0d3bf99fc532a9e746a94006a6bb9deba282ce8edd6ab91d41902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308371"
---
# <a name="vml-miterlimit-attribute"></a>Attributo VML MiterLimit

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce la levigazione dell'giunto miter. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *elemento* miterlimit=" *espressione* ">

**Sintassi dello script**

*element* .miterlimit="*expression*"

*expression* = *elemento*.miterlimit

**Osservazioni:**

Distanza massima tra il punto interno e il punto esterno di un'giunzione. Questo numero è un multiplo dello spessore della linea.

Il valore predefinito è 8.

*Attributo standard VML*

**Esempio**

Le giunzioni sulla polilinea sono miste con un limite di 10, cio? 5 x 2 punti.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 