---
title: Attributo ID (Path)(VML)
description: Attributo ID (Path)(VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29fe87845616b0e93e47458cd5c96f25733edd3aea7b09af6088b057d8ce0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118845919"
---
# <a name="id-attribute-pathvml"></a>Attributo ID (Path)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Nome che fornisce un identificatore univoco per un percorso. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *element* id=" *expression* ">

**Sintassi dello script**

*element* .id="*expression*"

*expression* = *id dell'elemento*

**Osservazioni:**

Usare **l'ID** per fare riferimento a un percorso specifico. Dopo aver creato un percorso e aver assegnato un ID, è possibile usare il nome ID quando si vuole modificare il percorso.

*Attributo VML Standard*

**Esempio**

La forma ha un ID tracciato denominato "myPath".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 