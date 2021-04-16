---
title: Attributo title (Shape) (la)
description: Attributo title (Shape) (la)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474155"
---
# <a name="title-attribute-shapevml"></a>Attributo title (Shape) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il testo visualizzato quando il puntatore del mouse viene spostato sulla forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* title = " *Expression* " >

**Sintassi dello script**

*element* . title = "*espressione*"

*espressione* = *element*. title

**Osservazioni:**

L'attributo **title** è simile all'attributo del **titolo** HTML standard. Il comportamento di un titolo è simile a una descrizione comando di Microsoft Windows.

**Attributo standard la**

**Esempio**

Il titolo della forma è "visualizzazione Descrizione comando" e verrà visualizzato quando il puntatore del mouse viene spostato sulla forma.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Esempio di attributo title](/previous-versions/bb264097(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 