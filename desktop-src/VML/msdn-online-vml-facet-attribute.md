---
title: Attributo facet la
description: Attributo facet la
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117954"
---
# <a name="vml-facet-attribute"></a>Attributo facet la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il numero di facet usati per descrivere le superfici curve di un'estrusione. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi Tag**

<o: *elemento* facet = " *Expression* " >

**Sintassi dello script**

*element* . facet = "*Expression*"

*espressione* = *elemento*. facet

**Osservazioni:**

Definisce la modalità di approssimazione dell'estrusione da parte di un motore di rendering. Un numero più basso indicherà una tolleranza di rendering inferiore al motore di rendering e produrrà un maggior numero di facet. I numeri più alti faranno apparire più sfaccettate l'estrusione. Il valore predefinito è 30.000.

*Attributo Microsoft Office Extensions*

 

 