---
title: Attributo VML ForceDash
description: Attributo VML ForceDash
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e162f95c4760c8a499f690c600fd651259694bae5c7fcc81ed2b2ee0d65bcb09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396066"
---
# <a name="vml-forcedash-attribute"></a>Attributo VML ForceDash

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se un contorno tratteggiato viene usato per disegnare una forma quando una forma non ha linee o riempimento. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* o:forcedash=" *espressione* ">

**Osservazioni:**

Usato da Microsoft PowerPoint segnaposto per disegnare un contorno tratteggiato quando non è presente alcuna linea e nessun riempimento per una forma. L'impostazione predefinita è **False**. Se **True,** verrà usato un contorno tratteggiato per indicare un segnaposto.

*Microsoft Office Attributo Extensions*

**Esempio**

Verrà usata una linea tratteggiata per eseguire il rendering della forma se non è presente alcuna linea o riempimento.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 