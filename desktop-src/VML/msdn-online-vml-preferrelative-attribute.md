---
title: Attributo VML PreferRelative
description: Attributo VML PreferRelative
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154297a528f18a3ac53f788ebbfe80ff59196f2872dd3dcb3789db16d5c91cb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654981"
---
# <a name="vml-preferrelative-attribute"></a>Attributo VML PreferRelative

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se le dimensioni originali di un oggetto vengono salvate dopo la riformattazione. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* o:preferrelative=" *expression* ">

**Osservazioni:**

Il valore predefinito è **False**. Se **True,** le dimensioni originali dell'oggetto verranno archiviate e tutte le dimensioni verranno ridimensionate in base a una percentuale di tale dimensione originale. In caso contrario, ogni ridimensionamento reimposta la scala su 100%.

*Microsoft Office Attributo Extensions*

**Esempio**

Se la forma viene ridimensionata, le dimensioni originali non verranno archiviate.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 