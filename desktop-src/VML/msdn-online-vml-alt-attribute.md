---
title: Attributo VML Alt
description: Attributo VML Alt
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08714efca9a390cbbec2f3dcf14782053d34db3506462214b9e62ebf1da206a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905341"
---
# <a name="vml-alt-attribute"></a>Attributo VML Alt

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il testo alternativo da visualizzare anziché un elemento grafico. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* alt=" *expression* ">

**Sintassi dello script**

*element* .alt="*expression*"

*expression* = *elemento*.alt

**Osservazioni:**

**L'attributo Alt** è simile all'attributo HTML **Alt** standard. Questo attributo consente ai browser di convertire il testo in voce per descrivere gli elementi grafici in una pagina.

*Attributo VML Standard*

**Vedere anche**

[Forma](shape-element--vml.md)

**Esempio**

**L'elemento ALT** seguente visualizza la frase "Rettangolo rosso" nei browser che convertono le pagine Web in frasi pronunciate.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo ALT.](/previous-versions/bb229663(v=vs.85)) Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 