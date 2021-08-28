---
title: Attributo ID (Shadow)(VML)
description: Attributo ID (Shadow)(VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44cc307bcdd381247a105cc447e920819d3e8877bf66a81088bc8eabc8fa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057919"
---
# <a name="id-attribute-shadowvml"></a>Attributo ID (Shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica un nome che fornisce un identificatore univoco per un'ombreggiatura. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* id=" *expression* ">

**Sintassi dello script**

*element* .id="*expression*"

*expression* = *id dell'elemento*

**Osservazioni:**

Usare **l'ID** per fare riferimento a un'ombreggiatura specifica. Dopo aver creato un'ombreggiatura e aver assegnato un ID, è possibile usare il nome ID quando si vuole modificare l'ombreggiatura.

*Attributo VML Standard*

**Esempio**

La forma ha un ID ombreggiatura denominato "myshadow".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 