---
title: Attributo Title (Shape)(VML)
description: Attributo Title (Shape)(VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ec2a16df6740bca64357dae039f4222de956300604198b2d199977970c526d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596509"
---
# <a name="title-attribute-shapevml"></a>Attributo Title (Shape)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il testo visualizzato quando il puntatore del mouse viene spostato sulla forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* title=" *expression* ">

**Sintassi dello script**

*element* .title="*expression*"

*expression* = *elemento*.title

**Osservazioni:**

**L'attributo Title** è simile all'attributo Html **Title** standard. Il comportamento di un titolo è simile a quello di una descrizione Windows Microsoft.

**Attributo VML Standard**

**Esempio**

Il titolo della forma è "Visualizzazione descrizione comando" e verrà visualizzato quando il puntatore del mouse si sposta sulla forma.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo Title](/previous-versions/bb264097(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 