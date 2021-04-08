---
title: Attributo color2 (Shadow) (la)
description: Attributo color2 (Shadow) (la)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729194"
---
# <a name="color2-attribute-shadowvml"></a>Attributo color2 (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il secondo colore di un'ombreggiatura. Proprietà di lettura/scrittura. **VgColor**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* color2 = " *Expression* " >

**Sintassi dello script**

*element* . color2 = "*Expression*"

*espressione* = *elemento*. color2

**Osservazioni:**

Usare un secondo colore per creare effetti speciali di ombreggiatura. Per ulteriori informazioni sui secondi colori, vedere l'attributo [Type](type-attribute--shadow--vml.md) .

*Attributo standard la*

**Esempio**

L'ombreggiatura è blu per un secondo colore.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 