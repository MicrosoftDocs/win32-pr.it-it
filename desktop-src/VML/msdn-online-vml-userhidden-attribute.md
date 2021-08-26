---
title: Attributo VML UserHidden
description: Attributo VML UserHidden
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb49b54c2463769286d11877e992bb30d4e431f351e39bf30b0ed6ab748a58e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959231"
---
# <a name="vml-userhidden-attribute"></a>Attributo VML UserHidden

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un ancoraggio di script è nascosto. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* o:userhidden=" *expression* ">

**Osservazioni:**

Il valore predefinito è **False**. Se **True,** gli ancoraggi dello script rimangono nascosti anche se la forma è altrimenti visibile.

*Microsoft Office Attributo Extensions*

**Esempio**

L'ancoraggio dello script della forma è nascosto.


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 