---
title: Attributo VML BWNormal
description: Attributo VML BWNormal
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754956"
---
# <a name="vml-bwnormal-attribute"></a>Attributo VML BWNormal

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la modalità in bianco e nero per i normali dispositivi di output in bianco e nero. Proprietà di lettura/scrittura. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* o:bwnormal=" *expression* ">

**Osservazioni:**

Quando [BWMode è](msdn-online-vml-bwmode-attribute.md) impostato su **auto,** questo attributo viene usato per determinare come eseguire il rendering della forma in bianco e nero normale.

Per altre informazioni sui valori di questo attributo, vedere [l'argomento VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) Il valore predefinito è **auto**.

*Microsoft Office Attributo Extensions*

**Esempio**

La forma viene elaborata come immagine in scala di grigi per il normale output in bianco e nero.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 