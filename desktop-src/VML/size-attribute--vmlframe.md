---
title: Attributo Size (VMLFrame)
description: Attributo Size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754126"
---
# <a name="size-attribute-vmlframe"></a>Attributo Size (VMLFrame)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce le dimensioni dell'area di ritaglio del fotogramma. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi dei tag**

<v: *element* size=" *expression* ">

**Sintassi dello script**

*element* .size="*expression*"

*expression* = *elemento*.size

**Osservazioni:**

Il valore predefinito è 0,0. Si noti **che Size** funziona solo se [Clip](msdn-online-vml-clip-attribute.md) è **True.** In questo attributo le dimensioni sono definite come larghezza e altezza del frame.

*Attributo standard VML*

**Esempio**

Le dimensioni dell'area di ritaglio saranno di 50 pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 