---
title: Attributo Layout-Flow VML
description: Attributo Layout-Flow VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde6937a3f93ff2a462cfc5950c13b7f3910573c54d82449ef705bca4afbb068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599355"
---
# <a name="vml-layout-flow-attribute"></a>Attributo Layout-Flow VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina il flusso del layout del testo in una casella di testo. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintassi dei tag**

<v: *element* style="layout-flow: *expression* ">

**Osservazioni:**

I possibili valori sono:



| Valore                  | Descrizione                                 |
|------------------------|---------------------------------------------|
| orizzontale             | Il testo viene visualizzato orizzontalmente. Valore predefinito.    |
| Verticale               | Il testo viene visualizzato verticalmente.               |
| ideografico verticale   | Il testo ideografico viene visualizzato verticalmente.   |
| ideografico orizzontale | Il testo ideografico viene visualizzato orizzontalmente. |



 

*Attributo standard VML*

**Esempio**

Il flusso di testo nella casella di testo scorrerà verticalmente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 