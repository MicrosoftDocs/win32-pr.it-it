---
title: Attributo ID (TextBox)(VML)
description: Attributo ID (TextBox)(VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a3a7e88c847cf63a1362d43cb6acaf21a548b141b71ffd2724c779f8eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099291"
---
# <a name="id-attribute-textboxvml"></a>Attributo ID (TextBox)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Nome che fornisce un identificatore univoco per una casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi dei tag**

<v: *element* id=" *expression* ">

**Sintassi dello script**

*element* .id="*expression*"

*expression* = *id dell'elemento*

**Osservazioni:**

Usare **l'ID** per fare riferimento a una casella di testo specifica. Dopo aver creato una casella di testo e aver assegnato un ID, è possibile usare il nome ID quando si vuole modificare la casella di testo.

*Attributo VML Standard*

**Esempio**

La forma ha un ID casella di testo denominato "mytextbox".


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



 

 