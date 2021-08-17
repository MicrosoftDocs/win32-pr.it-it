---
title: Attributo di stile VML
description: Attributo di stile VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0b7ce7985687d560fc46ebb98d41b51e7a461e811deb228b0a5709a35c5d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475191"
---
# <a name="vml-style-attribute"></a>Attributo di stile VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce lo stile del frame. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi dei tag**

<v: *element* style=" *expression* ">

**Sintassi dello script**

*element* .style="*expression*"

*expression* = *elemento*.style

**Osservazioni:**

Questo attributo usa i normali attributi di stile CSS per il posizionamento.

*Attributo standard VML*

**Esempio**

Lo stile definisce la posizione effettiva del frame.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 