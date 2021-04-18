---
title: Attributo del metodo la
description: Attributo del metodo la
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300140"
---
# <a name="vml-method-attribute"></a>Attributo del metodo la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il metodo utilizzato per generare un riempimento sfumato. Proprietà di lettura/scrittura. **VgSigmaType**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* Method = " *Expression* " >

**Sintassi dello script**

*element* . Method = "*Expression*"

*espressione* = *element*. Method

**Osservazioni:**

I possibili valori sono:



| Valore  | Descrizione          |
|--------|----------------------|
| nessuno   | Nessun riempimento Sigma.       |
| Lineari | Riempimento Sigma lineare.   |
| Sigma  | Riempimento Sigma. Valore predefinito. |
| Qualsiasi    | Qualsiasi riempimento Sigma.      |



 

*Attributo standard la*

**Esempio**

La forma avrà un riempimento sfumato lineare rosso.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 