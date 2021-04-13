---
title: Attributo position (Shape) (la)
description: Attributo position (Shape) (la)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399674"
---
# <a name="position-attribute-shapevml"></a>Attributo position (Shape) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il tipo di posizionamento utilizzato per inserire un elemento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "position: *Expression* " >

**Sintassi dello script**

*element* . Style. Position = "*espressione*"

*espressione* = *element*. Style. Position

**Osservazioni:**

L'attributo **position** è simile all'attributo **position** HTML standard usato con i fogli di stile.

I possibili valori sono:



| Valore    | Descrizione                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Valore predefinito. L'elemento viene posizionato in base al normale flusso della pagina. Gli attributi **Top** e **Left** vengono ignorati. Se l'oggetto è ancorato inline, che si verifica solo in Microsoft Word, viene usato questo valore. |
| assoluto | L'elemento è posizionato in relazione al padre, usando gli attributi **Top** e **Left** . Questo valore viene utilizzato dagli oggetti mobili di Microsoft Word e Microsoft Excel e dalle diapositive di Microsoft PowerPoint.                  |
| relative | L'elemento viene posizionato in base al normale flusso della pagina, ma vengono utilizzati gli attributi **Top** e **Left** . La sovrapposizione di elementi sovrapposti è regolata dall'attributo **Z-index** .                       |



 

*Attributo standard la*

**Esempio**

La posizione del rettangolo viene visualizzata utilizzando lo stile *relativo* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo position](/previous-versions/bb264090(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 