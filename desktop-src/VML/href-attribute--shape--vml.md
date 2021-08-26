---
title: Attributo HRef (Shape)(VML)
description: Attributo HRef (Shape)(VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe4b545aa27d311b0e1d0c73f0107aa6fdb357d524d3150ce6ab7dfb1e0f009
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072041"
---
# <a name="href-attribute-shapevml"></a>Attributo HRef (Shape)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce un URL per una forma. Quando si fa clic sulla forma, il browser carica l'URL. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* href=" *espressione* ">

**Sintassi dello script**

*element* .href="*expression*"

*expression* = *elemento*.href

**Osservazioni:**

**L'attributo HRef** è simile all'attributo **HRef HTML** standard degli ancoraggi.

**L'uso di HRef** semplifica la creazione di pulsanti interessanti in una pagina Web.

*Attributo standard VML*

**Esempio**

Quando si fa clic sul rettangolo, il browser carica il Microsoft Corporation home page.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Esempio di attributo HRef](/previous-versions/bb229672(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 