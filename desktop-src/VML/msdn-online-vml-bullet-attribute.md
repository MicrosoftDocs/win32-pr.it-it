---
title: Attributo Bullet la
description: Attributo Bullet la
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399247"
---
# <a name="vml-bullet-attribute"></a>Attributo Bullet la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se una forma è un punto elenco grafico. **VgTriState** di lettura/scrittura.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:Bullet = " *Expression* " >

**Osservazioni:**

Il valore predefinito è **False**. Se **true**, la forma è un punto elenco grafico.

*Attributo Microsoft Office Extensions*

**Esempio**

La forma è un punto elenco.


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 