---
title: Attributo di visibilità la
description: Attributo di visibilità la
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299954"
---
# <a name="vml-visibility-attribute"></a>Attributo di visibilità la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se una forma viene visualizzata. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "Visibility: *Expression* " >

**Sintassi dello script**

*element* . Style. Visibility = "*Expression*"

*espressione* = *element*. Style. Visibility

**Osservazioni:**

L'attributo **visibility** è simile all'attributo di **visibilità** HTML standard per gli stili.

I possibili valori sono:



| Valore    | Descrizione                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | La forma è visibile.                                                                                                                                                                   |
| hidden   | La forma non è visibile, ma fa ancora parte del flusso degli oggetti nel browser. Gli eventi del mouse non vengono elaborati.                                                                  |
| inherit  | Valore predefinito. Lo stato di visibilità viene ereditato dall'elemento padre della forma. Le applicazioni Microsoft Office utilizzano solo **ereditarietà** e **Hidden**; tutti gli altri valori vengono mappati per **ereditare**. |
| comprimere | Utilizzato per le applicazioni di modifica grafica che possono comprimere gruppi di forme; ad esempio, i delineatori.                                                                                     |



 

*Attributo standard la*

**Esempio**

Il codice seguente crea una forma, ma la rende nascosta. Il flusso di altri oggetti nel documento verrà aggirato, lasciando uno spazio delle stesse dimensioni della forma.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Esempio di attributo Visibility](/previous-versions/bb264100(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 