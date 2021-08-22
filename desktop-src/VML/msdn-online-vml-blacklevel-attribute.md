---
title: Attributo VML BlackLevel
description: Attributo VML BlackLevel
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe31c9507468efd27aac9d9729a4f2ee3ddce449398b4a68bd7d79b2d029b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057909"
---
# <a name="vml-blacklevel-attribute"></a>Attributo VML BlackLevel

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'intensità del nero in un'immagine. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *elemento* blacklevel=" *espressione* ">

**Sintassi dello script**

*element* .blacklevel="*expression*"

*expression* = *elemento*.blacklevel

**Osservazioni:**

Consente di modificare il livello del colore in modo che i nere vengano visualizzati come neri veri e tutti gli altri colori siano visibili come sfumature sopra il nero. Il valore predefinito è 0. Sebbene sia consentito qualsiasi numero compreso tra l'infinito positivo e negativo, i valori minori di -0,5 verranno visualizzati come tutti i valori neri e quelli maggiori di 0,5 verranno visualizzati come tutti bianchi.

*Attributo VML Standard*

**Esempio**

L'immagine verrà visualizzata con toni molto scuri.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 