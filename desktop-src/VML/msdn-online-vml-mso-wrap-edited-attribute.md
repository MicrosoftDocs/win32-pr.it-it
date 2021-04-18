---
title: La MSO-attributo modificato a capo
description: La MSO-attributo modificato a capo
ms.assetid: cb0e8618-e649-4a3c-9433-2be77c4b65f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a272a56b57d82ca0fee9f69fbde2757316439fd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300005"
---
# <a name="vml-mso-wrap-edited-attribute"></a>La MSO-attributo modificato a capo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se le coordinate a capo sono state personalizzate dall'utente. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* Style = "MSO-wrap-Edited: *Expression* " >

**Osservazioni:**

Se le coordinate a capo vengono generate da un editor, questo attributo è **true**; in caso contrario, sono stati personalizzati da un utente.

*Attributo Microsoft Office Extensions*

**Esempio**

Le coordinate a capo della forma sono state generate da un editor di forme.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-edited:True"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 