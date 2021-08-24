---
title: Attributo Origin (VMLFrame)(VML)
description: Attributo Origin (VMLFrame)(VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874b857a2408927e296f82f0f9aa0a5e15f6da69b1e2af6eaf6ebe2c5df746d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768261"
---
# <a name="origin-attribute-vmlframevml"></a>Attributo Origin (VMLFrame)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'origine dell'area di ritaglio del fotogramma. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi dei tag**

<v: *element* origin=" *expression* ">

**Sintassi dello script**

*element* .origin="*expression*"

*expression* = *elemento*.origin

**Osservazioni:**

Il valore predefinito è 0,0. Si noti **che Origin** funziona solo se [Clip](msdn-online-vml-clip-attribute.md) è **True.** In questo attributo l'origine è definita come l'angolo superiore sinistro del frame.

*Attributo standard VML*

**Esempio**

L'origine dell'area di ritaglio è 100pt,100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 