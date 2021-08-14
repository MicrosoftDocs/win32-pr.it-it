---
title: Attributo di visibilità VML
description: Attributo di visibilità VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2087a8c5915b400f32f6007d58c5c20344f9abab1e2c5bc5d4c93da74ddf1182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346183"
---
# <a name="vml-visibility-attribute"></a>Attributo di visibilità VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se viene visualizzata una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="visibility: *expression* ">

**Sintassi dello script**

*element* .style.visibility="*expression*"

*expression* = *elemento*.style.visibility

**Osservazioni:**

**L'attributo Visibility** è simile all'attributo **Visibility** HTML standard per gli stili.

I possibili valori sono:



| Valore    | Descrizione                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | La forma è visibile.                                                                                                                                                                   |
| hidden   | La forma non è visibile, ma fa ancora parte del flusso degli oggetti nel browser. Gli eventi del mouse non vengono elaborati.                                                                  |
| inherit  | Valore predefinito. Lo stato di visibilità viene ereditato dall'elemento padre della forma. Microsoft Office applicazioni usano solo **ereditare** e **nascondere**; Viene eseguito il mapping di qualsiasi altro valore per **ereditare**. |
| comprimere | Usato per le applicazioni di modifica grafica in grado di comprimere gruppi di forme; ad esempio, strutture.                                                                                     |



 

*Attributo VML Standard*

**Esempio**

Il codice seguente crea una forma, ma la rende nascosta. Altri oggetti nel documento scorreranno intorno ad esso, lasciando uno spazio delle stesse dimensioni della forma.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Esempio di attributo di visibilità](/previous-versions/bb264100(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 