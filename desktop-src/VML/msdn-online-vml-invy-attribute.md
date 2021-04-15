---
title: Attributo InvY di la
description: Attributo InvY di la
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338007"
---
# <a name="vml-invy-attribute"></a>Attributo InvY di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se la posizione y dell'handle è invertita. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[H](msdn-online-vml-h-element.md) (sottoelemento di [Handles](msdn-online-vml-handles-element.md))

**Sintassi Tag**

<v: *element* invy = " *Expression* " >

**Osservazioni:**

Se è **true**, la posizione y dell'handle viene invertita sottraendo il valore y dal valore y di **CoordOrigin** aggiunto al valore y di **CoordSize**. Il valore predefinito è **False**.

Questo attributo è l'equivalente di


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Attributo standard la*

 

 