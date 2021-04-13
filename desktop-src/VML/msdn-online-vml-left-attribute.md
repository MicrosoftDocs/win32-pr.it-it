---
title: Attributo la Left
description: Attributo la Left
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474027"
---
# <a name="vml-left-attribute"></a>Attributo la Left

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina la posizione della forma rispetto all'elemento a sinistra del flusso del documento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "Left: *Expression* " >

**Sintassi dello script**

*element* . Style. Left = "*Expression*"

*espressione* = *element*. Style. Left

**Osservazioni:**

L'attributo **Left** è simile all'attributo HTML **Left** standard per gli stili.

È possibile eseguire il mapping delle unità all'elemento padre oppure in unità assolute. Questo attributo non verrà scritto per le forme ancorate inline.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                          |
| units      | Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, viene utilizzato pixels (px). |
| percentuale | Valore espresso come percentuale della larghezza dell'oggetto padre.                                                                                                    |



 

*Attributo standard la*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

Il valore sinistro della forma è impostato su 1 nell'esempio riportato di seguito.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 