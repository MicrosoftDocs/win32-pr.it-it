---
title: Attributo GradientShapeOK di la
description: Attributo GradientShapeOK di la
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399629"
---
# <a name="vml-gradientshapeok-attribute"></a>Attributo GradientShapeOK di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un percorso sfumato sarà costituito da percorsi concentrici ripetuti. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* gradientshapeok = " *Expression* " >

**Sintassi dello script**

*element* . gradientshapeok = "*Expression*"

*espressione* = *elemento*. gradientshapeok

**Osservazioni:**

Se **true**, il percorso verrà riempito con un riempimento di sfumatura concentrico usando il tracciato come forma ripetuta della sfumatura. Il valore predefinito è **false**.

*Attributo standard la*

**Esempio**

Il percorso verrà riempito con un riempimento sfumato concentrico costituito da rettangoli ripetuti.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 