---
title: Attributo Margin-Top la
description: Attributo Margin-Top la
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339167"
---
# <a name="vml-margin-top-attribute"></a>Attributo Margin-Top la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica il bordo superiore del rettangolo che lo contiene della forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* margin-top = " *Expression* " >

**Sintassi dello script**

*element* . margin-top = "*Expression*"

*espressione* = *elemento*. margin-top

**Osservazioni:**

L'attributo **margin-top** è simile all'attributo standard **margin-top** HTML usato con i fogli di stile.

Si noti che viene usato **MarginTop** anziché **margin-top** per lo scripting. Si noti inoltre che se la **posizione** è **assoluta**, il margine non verrà modificato.

Questa proprietà viene usata al posto di **Top** per le forme in Microsoft Word e Microsoft Excel che si trovano in una posizione relativa a un punto di ancoraggio.

I possibili valori sono:



| Valore      | Descrizione                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posizione predefinita di un elemento nel flusso della pagina.                                                                                                                                           |
| units      | Valore predefinito. Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex). Se non viene specificata alcuna unità, viene utilizzato pixels (px). Il valore predefinito è 0. |
| percentuale | Valore espresso come percentuale dell'altezza dell'oggetto padre.                                                                                                                                    |



 

*Attributo standard la*

**Vedere anche**

[Unità](msdn-online-vml-units.md)

**Esempio**

Il margine superiore è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Esempio di attributo margin-top](/previous-versions/bb264087(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 