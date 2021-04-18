---
title: Attributo position (H) (la)
description: Attributo position (H) (la)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300360"
---
# <a name="position-attribute-hvml"></a>Attributo position (H) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica i valori theX e y dell'handle. **VgVector2D** di lettura/scrittura.

**Si applica a**

[H](msdn-online-vml-h-element.md) (sottoelemento di [Handles](msdn-online-vml-handles-element.md))

**Sintassi Tag**

<v: *elemento* position = " *Expression* " >

**Osservazioni:**

i valori x e y possono essere di uno dei tipi seguenti:

-   constant
-   Formula (ad esempio, @2 )
-   regolare (ad esempio, \# 3)
-   center
-   TopLeft
-   BottomRight

Se viene specificato uno dei tipi precedenti eccetto *Adjust* , la posizione dell'handle è fissa in tale dimensione. Se viene specificato un handle di regolazione, l'handle è libero di spostarsi in tale dimensione e il valore di regolazione è determinato dalla posizione dell'handle.

Se viene specificato un attributo [polare](msdn-online-vml-polar-attribute.md) , l'attributo **position** rappresenta il raggio e i valori angolo dell'handle anziché x e y.

Il valore predefinito è 0,0.

*Attributo standard la*

 

 