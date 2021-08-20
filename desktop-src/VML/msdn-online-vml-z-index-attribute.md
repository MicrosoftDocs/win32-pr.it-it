---
title: Attributo VML Z-Index
description: Attributo VML Z-Index
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07100b2ecdbda792ea3f7d5550759430539b95b86c5ef76ded2f9238785b1151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123771"
---
# <a name="vml-z-index-attribute"></a>Attributo VML Z-Index

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina l'ordine di visualizzazione delle forme sovrapposte. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="z-index: *expression* ">

**Sintassi dello script**

*element* .style.zindex="*expression*"

*expression* = *elemento*.style.zindex

**Osservazioni:**

**L'attributo Z-Index** è simile all'attributo **Z-Index** HTML standard per gli stili.

I possibili valori sono:



| Valore | Descrizione                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto  | L'ordine in cui le forme vengono visualizzate nella pagina HTML verrà usato, dal basso verso l'alto.                                                                                                                         |
| order | Numero che rappresenta la precedenza di sovrapposizione. Una forma con un numero maggiore verrà visualizzata come se fosse sovrapposta (davanti) a una forma con un numero inferiore. È possibile usare numeri negativi. |



 

*Attributo VML Standard*

**Esempio**

La forma rossa verrà visualizzata nella parte anteriore della forma blu, perché ha un indice z superiore.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Esempio di attributo Z-Index](/previous-versions/ms530275(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 