---
title: Attributo di opacità (ombreggiatura)(VML)
description: Attributo di opacità (ombreggiatura)(VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43287a4bb6de9f2dd0d9d2b0af97d971314ab7e93ab2c4fae58b666ee1a94124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680621"
---
# <a name="opacity-attribute-shadowvml"></a>Attributo di opacità (ombreggiatura)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina la trasparenza di un'ombreggiatura. Proprietà di lettura/scrittura. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* opacity=" *expression* ">

**Sintassi dello script**

*element* .opacity="*expression*"

*expression* = *opacità* dell'elemento

**Osservazioni:**

Il valore predefinito è 1. Il valore 0 crea un'ombreggiatura completamente trasparente.

*Attributo VML Standard*

**Esempio**

La forma ha un'ombreggiatura trasparente al 50%.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 