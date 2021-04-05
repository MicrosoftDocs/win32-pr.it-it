---
title: LA attributo Top
description: LA attributo Top
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728242"
---
# <a name="vml-top-attribute"></a>LA attributo Top

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la posizione della forma rispetto all'elemento sopra di esso nel flusso della pagina. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "Top: *Expression* " >

**Sintassi dello script**

*element* . Style.Top = "*Expression*"

*espressione* = *elemento*. Style.Top

**Osservazioni:**

L'attributo **Top** è simile all'attributo **Top** HTML standard per gli stili.

È possibile eseguire il mapping delle unità all'elemento padre oppure in unità assolute. Questo attributo non può essere scritto per forme ancorate inline.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                          |
| units      | Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, viene utilizzato pixels (px). |
| percentuale | Valore espresso come percentuale dell'altezza dell'oggetto padre.                                                                                                   |



 

*Attributo standard la*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

Il bordo superiore della forma è 5 pixel sotto l'oggetto che lo precede nel flusso della pagina.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo Top](/previous-versions/bb264098(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 