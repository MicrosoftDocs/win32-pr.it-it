---
title: Attributo clip VML
description: Attributo clip VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999291"
---
# <a name="vml-clip-attribute"></a>Attributo clip VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se il ritaglio è on. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi dei tag**

<v: *elemento* clip=" *espressione* ">

**Sintassi dello script**

*elemento* .clip="*expression*"

*expression* = *elemento*.clip

**Osservazioni:**

Se **Clip** è **False,** la forma verrà ridimensionata in base al frame. Se **True,** tutte le parti della forma esterne al frame non verranno visualizzate.

Si noti [che Origin](origin-attribute--vmlframe--vml.md) e [Size](size-attribute--vmlframe.md) non verranno usati a meno **che Clip** non sia **True.**

*Attributo standard VML*

**Esempio**

L'immagine definita nel file esterno verrà ritagliata.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 