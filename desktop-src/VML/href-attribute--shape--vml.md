---
title: Attributo HRef (Shape) (la)
description: Attributo HRef (Shape) (la)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047270"
---
# <a name="href-attribute-shapevml"></a>Attributo HRef (Shape) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un URL per una forma. Quando si fa clic sulla forma, il browser caricherà l'URL. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* href = " *Expression* " >

**Sintassi dello script**

*element* . href = "*Expression*"

*espressione* = *elemento*. href

**Osservazioni:**

L'attributo **href** è simile all'attributo HTML **href** standard degli ancoraggi.

L'uso di **href** consente di creare facilmente pulsanti interessanti in una pagina Web.

*Attributo standard la*

**Esempio**

Quando si fa clic sul rettangolo, il browser caricherà il home page Microsoft Corporation.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Esempio di attributo href](/previous-versions/bb229672(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 