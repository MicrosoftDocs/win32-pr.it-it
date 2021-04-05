---
title: Attributo INSERT la
description: Attributo INSERT la
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117906"
---
# <a name="vml-inset-attribute"></a>Attributo INSERT la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica i valori del margine interno per il testo della casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi Tag**

<v: *elemento* Insert = " *Expression* " >

**Sintassi dello script**

*element* . Insert = "*Expression*"

*espressione* = *elemento*. Insert

**Osservazioni:**

Il valore del margine interno del testo viene specificato come stringa contenente quattro valori, separati da virgole o spazi. I valori misurano l'incasso dai bordi sinistro, superiore, destro e inferiore della casella specificata dall'attributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) di **path**. I valori mancanti vengono impostati sul valore predefinito, ovvero "0.1 in, 0,05 in, 0.1 in, 0,05 in".

Per le forme ruotate nei browser che non supportano la rotazione, il rettangolo di delimitazione viene agganciato al multiplo più vicino di 90 gradi.

*Attributo standard la*

**Esempio**

La casella di testo avrà un margine interno di 10 pixel.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 