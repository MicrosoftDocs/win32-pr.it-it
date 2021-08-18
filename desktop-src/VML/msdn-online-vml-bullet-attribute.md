---
title: Attributo VML Bullet
description: Attributo VML Bullet
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f35fda917931567dcd2dc4cf823ed74e3b449e05fba6046f1390e3d6454fd45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755020"
---
# <a name="vml-bullet-attribute"></a>Attributo VML Bullet

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se una forma è un punto elenco grafico. VgTriState di **lettura/scrittura.**

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* o:bullet=" *espressione* ">

**Osservazioni:**

Il valore predefinito è **False**. Se **True**, la forma è un punto elenco grafico.

*Microsoft Office Attributo Extensions*

**Esempio**

La forma è un punto elenco.


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 