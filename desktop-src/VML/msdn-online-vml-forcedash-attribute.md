---
title: Attributo ForceDash di la
description: Attributo ForceDash di la
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047054"
---
# <a name="vml-forcedash-attribute"></a>Attributo ForceDash di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un contorno tratteggiato viene utilizzato per disegnare una forma quando una forma non ha linea o riempimento. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:forcedash = " *Expression* " >

**Osservazioni:**

Utilizzato dai segnaposto di Microsoft PowerPoint per disegnare un contorno tratteggiato quando non è presente alcuna riga e nessun riempimento per una forma. L'impostazione predefinita è **False**. Se **true**, viene usato un contorno tratteggiato per indicare un segnaposto.

*Attributo Microsoft Office Extensions*

**Esempio**

Una linea tratteggiata verrà utilizzata per eseguire il rendering della forma se non è presente alcuna linea o riempimento.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 