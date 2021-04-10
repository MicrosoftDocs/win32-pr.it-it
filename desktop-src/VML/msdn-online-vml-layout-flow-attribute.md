---
title: Attributo Layout-Flow la
description: Attributo Layout-Flow la
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963245"
---
# <a name="vml-layout-flow-attribute"></a>Attributo Layout-Flow la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina il flusso del layout del testo in una casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi Tag**

<v: *elemento* Style = "layout-Flow: *Expression* " >

**Osservazioni:**

I possibili valori sono:



| Valore                  | Descrizione                                 |
|------------------------|---------------------------------------------|
| orizzontale             | Il testo viene visualizzato orizzontalmente. Valore predefinito.    |
| verticale               | Il testo viene visualizzato verticalmente.               |
| ideogrammi verticali   | Il testo ideogrammi viene visualizzato verticalmente.   |
| ideogrammi orizzontali | Il testo ideogrammi viene visualizzato orizzontalmente. |



 

*Attributo standard la*

**Esempio**

Il flusso di testo nella casella di testo viene propagato verticalmente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 