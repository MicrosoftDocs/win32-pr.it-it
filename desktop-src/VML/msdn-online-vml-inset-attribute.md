---
title: Attributo VML Inset
description: Attributo VML Inset
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1d4b44756034a3ebc7e46e1cdda43042f347e58cb87c02b00c90a14320a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600237"
---
# <a name="vml-inset-attribute"></a>Attributo VML Inset

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica i valori del margine interno per il testo della casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi dei tag**

<v: *element* inset=" *expression* ">

**Sintassi dello script**

*element* .inset="*expression*"

*expression* = *elemento*.inset

**Osservazioni:**

Il valore del margine di testo interno viene specificato come stringa contenente quattro valori, ognuno separato da virgole o spazi. I valori misurano l'inizio dei bordi sinistro, superiore, destro e inferiore della casella specificata [dall'attributo TextBoxRect](msdn-online-vml-textboxrect-attribute.md) di **Path.** I valori mancanti vengono impostati sul valore predefinito, ovvero "0.1in, 0.05in, 0.1in, 0.05in".

Per le forme ruotate nei browser che non supportano la rotazione, il rettangolo di selezione verrà allineato al multiplo più vicino di 90 gradi.

*Attributo VML Standard*

**Esempio**

La casella di testo avrà un margine iniziale di 10 pixel.


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



 

 