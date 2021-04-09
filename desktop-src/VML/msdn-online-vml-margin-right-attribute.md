---
title: Attributo Margin-Right la
description: Attributo Margin-Right la
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047336"
---
# <a name="vml-margin-right-attribute"></a>Attributo Margin-Right la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica il bordo destro del rettangolo che lo contiene della forma rispetto all'ancoraggio della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "margin-right: *Expression* " >

**Sintassi dello script**

*element* . Style. MarginRight = "*Expression*"

*espressione* = *element*. Style. MarginRight

**Osservazioni:**

L'attributo **margin-right** è simile all'attributo standard **margin-right** HTML usato con i fogli di stile.

Si noti che viene usato **MarginRight** anziché **margin-right** per lo scripting. Si noti inoltre che se la **posizione** è **assoluta**, il margine non verrà modificato.

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

Il margine destro è impostato su 25 pixel.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Esempio di attributo margin-right](/previous-versions/bb229677(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 