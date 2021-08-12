---
title: Attributo della classe VML
description: Attributo della classe VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ada95b56430dacd09801a9aaa200c92abab064bbbb5732b369372de63c34de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602184"
---
# <a name="vml-class-attribute"></a>Attributo della classe VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Fa riferimento a una definizione di uno stile CSS. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* class=" *expression* ">

**Sintassi dello script**

*element* .classname="*expression*"

*expression* = *elemento*.classname

**Osservazioni:**

**L'attributo** della classe è simile all'attributo **della classe** HTML standard usato con i fogli di stile CSS.

Si noti che **classname** viene usato al posto della **classe per** lo scripting. Si noti anche che per lo scripting, **il nome della classe** può essere solo letto. la modifica del valore **di classname** non modificherà il rendering della forma.

*Attributo VML Standard*

**Vedere anche**

[Forma](shape-element--vml.md)

**Esempio**

Viene creata una **classe per width** con lo stile


```HTML
   .narrowstyle {width:50;height:100}
```



Viene quindi fatto riferimento alla larghezza includendo lo stile . Si noti che la larghezza eheight non sono definite nell'attributo **di** stile, ma verranno definite dallo stile.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Si noti **che La classe** si applica solo agli attributi di tipo CSS.

 

 