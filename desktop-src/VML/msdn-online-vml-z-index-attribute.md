---
title: LA-attributo Z-index
description: LA-attributo Z-index
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963148"
---
# <a name="vml-z-index-attribute"></a>LA-attributo Z-index

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina l'ordine di visualizzazione delle forme sovrapposte. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "z-index: *Expression* " >

**Sintassi dello script**

*element* . Style. ZIndex = "*Expression*"

*espressione* = *element*. Style. ZIndex

**Osservazioni:**

L'attributo **z-index** è simile all'attributo standard HTML **z-index** per gli stili.

I possibili valori sono:



| Valore | Descrizione                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto  | Verrà utilizzato l'ordine in cui vengono visualizzate le forme nella pagina HTML, dal basso verso l'alto.                                                                                                                         |
| order | Numero che rappresenta la precedenza di sovrapposizione. Una forma con un numero più alto verrà visualizzata come se wereoverlapping (in "front" di) una forma con un numero inferiore. È possibile usare i numeri negativi. |



 

*Attributo standard la*

**Esempio**

La forma rossa verrà visualizzata in "anteriore" della forma blu, perché ha un indice z superiore.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Esempio di attributo Z-index](/previous-versions/ms530275(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 