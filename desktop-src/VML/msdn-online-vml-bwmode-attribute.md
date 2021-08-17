---
title: Attributo VML BWMode
description: Attributo VML BWMode
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5640680af40f4649f7ab34b2ec8cfd4e5cf94ee4c7c6ce3c3f2185e68bdac360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754966"
---
# <a name="vml-bwmode-attribute"></a>Attributo VML BWMode

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina il modo in cui verrà eseguito il rendering di una forma per i dispositivi di output in bianco e nero. Proprietà di lettura/scrittura. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* o:bwmode=" *expression* ">

**Osservazioni:**

Quando una forma viene stampata su una stampante in bianco e nero o visualizzata in una visualizzazione in bianco e nero in un'applicazione, sono possibili diverse opzioni. Per altre informazioni sui valori di questo attributo, vedere [l'argomento VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) Il valore predefinito è **auto**.

Se si imposta **auto,** viene usato [BWNormal](msdn-online-vml-bwnormal-attribute.md) per determinare il comportamento per il normale output in bianco e nero e [BWPure](msdn-online-vml-bwpure-attribute.md) per determinare il comportamento per l'output in bianco e nero puro.

*Microsoft Office Attributo Extensions*

**Esempio**

La modalità in bianco e nero della forma è **auto.**


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 