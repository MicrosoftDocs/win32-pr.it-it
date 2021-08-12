---
title: Attributo vml left
description: Attributo vml left
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c067b15281277a85f707f6152fa855c51ee49aba439b16c009f6ff029139a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599289"
---
# <a name="vml-left-attribute"></a>Attributo vml left

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina la posizione della forma rispetto all'elemento a sinistra nel flusso del documento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="left: *expression* ">

**Sintassi dello script**

*element* .style.left="*expression*"

*expression* = *elemento*.style.left

**Osservazioni:**

**L'attributo Left** è simile all'attributo HTML **Left** standard per gli stili.

Le unità possono essere mappate all'elemento padre o essere in unità assolute. Questo attributo non verrà scritto per le forme ancorate inline.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                          |
| units      | Numero con un identificatore di unità assoluto (cm, mm, in, pt, pc o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, vengono utilizzati i pixel (px). |
| percentuale | Valore espresso come percentuale della larghezza dell'oggetto padre.                                                                                                    |



 

*Attributo VML Standard*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

Il valore sinistro della forma è impostato su 1 nell'esempio seguente.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 