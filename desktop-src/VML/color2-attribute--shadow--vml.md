---
title: Attributo Color2 (Shadow)(VML)
description: Attributo Color2 (Shadow)(VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241c7e0a620b6b5f2f54a8849779dcc905d027781fe38a5121ca74b6acbeac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655701"
---
# <a name="color2-attribute-shadowvml"></a>Attributo Color2 (Shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il secondo colore di un'ombreggiatura. Proprietà di lettura/scrittura. **VgColor**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* color2=" *expression* ">

**Sintassi dello script**

*element* .color2="*expression*"

*expression* = *elemento*.color2

**Osservazioni:**

Usare un secondo colore per creare effetti ombreggiati speciali. Per altre [informazioni sui](type-attribute--shadow--vml.md) secondi colori, vedere l'attributo Type.

*Attributo VML Standard*

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



 

 