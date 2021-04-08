---
title: Attributo ID (TextBox) (la)
description: Attributo ID (TextBox) (la)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872677"
---
# <a name="id-attribute-textboxvml"></a>Attributo ID (TextBox) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Nome che fornisce un identificatore univoco per una casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi Tag**

<v: *element* ID = " *Expression* " >

**Sintassi dello script**

*element* . ID = "*Expression*"

*espressione* = *elemento*. ID

**Osservazioni:**

Usare **ID** per fare riferimento a una casella di testo specifica. Dopo aver creato una casella di testo e avergli assegnato un ID, è possibile usare il nome ID quando si desidera modificare la casella di testo.

*Attributo standard la*

**Esempio**

La forma ha un ID TextBox denominato "TextBox".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 