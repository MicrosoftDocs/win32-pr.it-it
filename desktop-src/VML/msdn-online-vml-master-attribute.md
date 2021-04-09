---
title: Attributo Master la
description: Attributo Master la
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118426"
---
# <a name="vml-master-attribute"></a>Attributo Master la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un elemento **TipoForma** è un elemento Master. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TipoForma](msdn-online-vml-shapetype-element.md)

**Sintassi Tag**

<v: *element* o:Master = " *Expression* " >

**Osservazioni:**

Se **true**, la forma **TipoForma** viene sottoposta a rendering dal motore di rendering. Il valore predefinito è **False**.

*Attributo Microsoft Office Extensions*

**Esempio**

L'elemento **TipoForma** è una forma master.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 