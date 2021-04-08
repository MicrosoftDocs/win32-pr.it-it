---
title: Attributo Matrix (asimmetria) (la)
description: Attributo Matrix (asimmetria) (la)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047268"
---
# <a name="matrix-attribute-skewvml"></a>Attributo Matrix (asimmetria) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una trasformazione della prospettiva di una asimmetria. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Sfasamento](msdn-online-vml-skew-element.md)

**Sintassi Tag**

<o: *element* Matrix = " *Expression* " >

**Sintassi dello script**

*element* . Matrix = "*Expression*"

*espressione* = *element*. Matrix

**Osservazioni:**

La matrice è una stringa nel formato "SXX, SXY, SYX, SYY, px, py", dove s è scale, p è Perspective e x e y sono valori x e y. Se l' [offset](offset-attribute--skew--vml.md) è espresso in unità assolute, px e py si trovano nelle [unità](msdn-online-vml-units.md) Emu ^-1 (in caso contrario si tratta di una frazione inversa della dimensione della forma). Il valore predefinito è "1, 0, 0, 1, 0, 0".

*Attributo Microsoft Office Extensions*

 

 