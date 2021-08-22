---
title: Attributo Opacity (Fill)(VML)
description: Attributo Opacity (Fill)(VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ea4f539eb2386dae7b8e863c95556cf70400c320ee515897cf7f96a85fe3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057599"
---
# <a name="opacity-attribute-fillvml"></a>Attributo Opacity (Fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la trasparenza di un riempimento. Proprietà di lettura/scrittura. [VgFraction](msdn-online-vml-vgfraction-data-type.md).

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* opacity=" *expression* ">

**Sintassi dello script**

*element* .opacity="*expression*"

*expression* = *opacità* dell'elemento

**Osservazioni:**

Il valore predefinito è 1,0.

*Attributo VML Standard*

**Esempio**

Il riempimento della forma sarà trasparente al 50%.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 