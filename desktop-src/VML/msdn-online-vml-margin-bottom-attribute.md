---
title: Attributo Margin-Bottom la
description: Attributo Margin-Bottom la
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728823"
---
# <a name="vml-margin-bottom-attribute"></a>Attributo Margin-Bottom la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica il bordo inferiore del rettangolo che lo contiene della forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* margin-bottom = " *Expression* " >

**Sintassi dello script**

*element* . MarginBottom = "*Expression*"

*espressione* = *elemento*. MarginBottom

**Osservazioni:**

L'attributo **margin-bottom** è simile all'attributo **margin-bottom** HTML standard usato con i fogli di stile.

Si noti che **MarginBottom** viene usato al posto del **margine inferiore** per lo scripting. Si noti inoltre che se la **posizione** è **assoluta**, il margine non verrà modificato.

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

Il margine inferiore è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[Esempio di attributo margin-bottom](/previous-versions/bb229675(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 