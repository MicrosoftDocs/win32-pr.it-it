---
title: Attributo OnMouseOver di VML
description: Attributo OnMouseOver di VML
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999131"
---
# <a name="vml-onmouseover-attribute"></a>Attributo OnMouseOver di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Attiva un evento del mouse per una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* onmouseover=" *espressione* ">

**Osservazioni:**

Quando il puntatore del mouse si trova sulla forma, viene generato un evento "mouseover". Il valore viene generato usando la parola chiave **this** (come riferimento all'oggetto ) seguita dalla sintassi del modello a oggetti. Ad esempio, per modificare il colore di riempimento in rosso, usare quanto segue:

onmouseover="this.fillcolor='red'"

Si noti l'uso delle virgolette singole e doppie per impostare l'espressione.

*Attributo standard VML*

**Esempio**

Quando il puntatore del mouse si trova sulla forma, il colore di riempimento passa da rosso a verde.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Esempio di attributo OnMouseOver](/previous-versions/bb264088(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 