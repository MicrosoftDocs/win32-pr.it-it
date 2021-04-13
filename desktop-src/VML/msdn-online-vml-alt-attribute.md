---
title: LA alt-attributo
description: LA alt-attributo
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224008"
---
# <a name="vml-alt-attribute"></a>LA alt-attributo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il testo alternativo da visualizzare anziché un elemento grafico. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Alt = " *Expression* " >

**Sintassi dello script**

*element* . Alt = "*Expression*"

*espressione* = *elemento*. Alt

**Osservazioni:**

L'attributo **ALT** è simile all'attributo **ALT** HTML standard. Questo attributo fornisce un modo per i browser che convertono il testo in sintesi vocale per descrivere elementi grafici in una pagina.

*Attributo standard la*

**Vedere anche**

[Con forme](shape-element--vml.md)

**Esempio**

L'elemento **ALT** seguente visualizzerà la frase "Red Rectangle" nei browser che convertono le pagine Web in frasi vocali.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo ALT](/previous-versions/bb229663(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 