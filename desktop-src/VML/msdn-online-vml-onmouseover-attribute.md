---
title: LA onmouseover (attributo)
description: LA onmouseover (attributo)
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8318235b660f92f3d82b2dd8dd15e2192e97a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047265"
---
# <a name="vml-onmouseover-attribute"></a>LA onmouseover (attributo)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Attiva un evento del mouse per una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* onmouseover = " *Expression* " >

**Osservazioni:**

Un evento "MouseOver" viene generato quando il puntatore del mouse si trova sulla forma. Il valore viene generato tramite la parola chiave **this** , come riferimento all'oggetto, seguito dalla sintassi del modello a oggetti. Per modificare il colore di riempimento in rosso, ad esempio, usare il comando seguente:

onmouseover = "this. FillColor =' Red '"

Si noti l'uso delle virgolette singole e doppie per impostare l'espressione.

*Attributo standard la*

**Esempio**

Quando il puntatore del mouse si trova sulla forma, il colore di riempimento si trasforma da rosso a verde.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Esempio di attributo onmouseover](/previous-versions/bb264088(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 