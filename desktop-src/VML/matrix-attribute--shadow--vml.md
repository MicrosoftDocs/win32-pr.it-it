---
title: Attributo Matrix (Shadow) (la)
description: Attributo Matrix (Shadow) (la)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399631"
---
# <a name="matrix-attribute-shadowvml"></a>Attributo Matrix (Shadow) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce una trasformazione della prospettiva per un'ombreggiatura. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi Tag**

<v: *element* Matrix = " *Expression* " >

**Sintassi dello script**

*element* . Matrix = "*Expression*"

*espressione* = *element*. Matrix

**Osservazioni:**

Una matrice di trasformazione prospettica nel formato "SXX, SXY, SYX, SYY, px, py" WHERE s = scale e p = Perspective. Se l'offset è in unità assolute, il px, py si trova in unità di 1/Emu; in caso contrario, si tratta di una frazione inversa della dimensione della forma.

*Attributo standard la*

 

 