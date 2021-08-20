---
title: Attributo ID (Stroke)(VML)
description: Attributo ID (Stroke)(VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02fa8ad958315af58e2abfa6d374a6545cc1e3e171080ec29ac6a30600160184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125304"
---
# <a name="id-attribute-strokevml"></a>Attributo ID (Stroke)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Nome che fornisce un identificatore univoco per un tratto. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[infarto](msdn-online-vml-stroke-element.md)

**Sintassi dei tag**

<v: *element* id=" *expression* ">

**Sintassi dello script**

*element* .id="*expression*"

*expression* = *id dell'elemento*

**Osservazioni:**

Usare **l'ID** per fare riferimento a un tratto specifico. Dopo aver creato un tratto e aver assegnato un ID, è possibile usare il nome ID quando si vuole modificare il tratto.

*Attributo VML Standard*

**Esempio**

La forma ha un ID tratto denominato "mystroke".


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 