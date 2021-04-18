---
title: Attributo UserHidden di la
description: Attributo UserHidden di la
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299918"
---
# <a name="vml-userhidden-attribute"></a>Attributo UserHidden di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un ancoraggio di script è nascosto. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:userhidden = " *Expression* " >

**Osservazioni:**

Il valore predefinito è **False**. Se **true**, gli ancoraggi degli script rimaneno nascosti anche se la forma è altrimenti visibile.

*Attributo Microsoft Office Extensions*

**Esempio**

L'ancoraggio dello script della forma è nascosto.


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 