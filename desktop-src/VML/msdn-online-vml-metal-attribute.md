---
title: Attributo Metal la
description: Attributo Metal la
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399064"
---
# <a name="vml-metal-attribute"></a>Attributo Metal la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se la superficie della forma estrusa sarà simile a metal. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi Tag**

<o: *element* Metal = " *Expression* " >

**Sintassi dello script**

*element* . metal = "*Expression*"

*espressione* = *element*. Metal

**Osservazioni:**

Se impostato su **true**, questo attributo fa sì che la luce riflessa in modo speculare sia il colore del materiale anziché il colore della sorgente di luce, rendendo l'oggetto apparentemente più metallico. Per approssimare un materiale metallico è necessario che la specularità sia relativamente alta (circa 1,2) e che la diffusione sia relativamente bassa (circa 0,6). Il valore predefinito è **False**.

*Attributo Microsoft Office Extensions*

 

 