---
title: Attributo EXT (asimmetria) (la)
description: Attributo EXT (asimmetria) (la)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223951"
---
# <a name="ext-attribute-skewvml"></a>Attributo EXT (asimmetria) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la modalità di visualizzazione di una asimmetria. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Sfasamento](msdn-online-vml-skew-element.md)

**Sintassi Tag**

<o: *element* v:EXT = " *Expression* " >

**Sintassi dello script**

*element* . ext = "*Expression*"

*espressione* = *elemento*. ext

**Osservazioni:**

Questo attributo viene utilizzato per indicare agli editor grafici come elaborare l'elemento di **inclinazione** . I possibili valori sono:

-   **edit**
-   **Visualizza** (impostazione predefinita)
-   **backwardCompatible**

Se un'estensione è impostata per la **modifica**, può essere ignorata da un visualizzatore di software. Se impostato su **View**, il visualizzatore deve invece eseguire il rendering della rappresentazione bitmap.

*Attributo Microsoft Office Extensions*

 

 