---
title: Attributo WrapCoords di la
description: Attributo WrapCoords di la
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727962"
---
# <a name="vml-wrapcoords-attribute"></a>Attributo WrapCoords di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il poligono delimitatore che racchiude una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:wrapcoords = " *Expression* " >

**Osservazioni:**

Descrive un elenco delimitato da virgole di x e ycoordinates; ovvero "x1, Y1, X2, Y2, X3, Y3,..." Viene usato quando il testo viene racchiuso tra parentesi intorno a una forma. Il valore predefinito è **null** (una stringa vuota) finché l'attributo **MSO-Wrap-Mode** non è impostato su **Tight** o **through**.

*Attributo Microsoft Office Extensions*

**Esempio**

La forma presenta un rettangolo di delimitazione del testo di 5 unità di dimensioni maggiori rispetto al percorso.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 