---
title: Elemento curva VML
description: Elemento curva VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fd06480b0d4bcf062f1f64eb9fa0b22862cf2b338b2c2f5ea0bf1c3cd2a1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655531"
---
# <a name="vml-curve-element"></a>Elemento curva VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Forma della curva predefinita.

**Curve** usa gli [attributi a](to-attribute--curve--vml.md), [da](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md)e [control2.](msdn-online-vml-control2-attribute.md)

Di seguito è riportato il codice minimo necessario per produrre un'immagine.


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 