---
title: Attributo PreferRelative di la
description: Attributo PreferRelative di la
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046838"
---
# <a name="vml-preferrelative-attribute"></a>Attributo PreferRelative di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se le dimensioni originali di un oggetto vengono salvate dopo la riformattazione. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:preferrelative = " *Expression* " >

**Osservazioni:**

Il valore predefinito è **False**. Se **true**, le dimensioni originali dell'oggetto verranno archiviate e tutto il ridimensionamento sarà basato su una percentuale delle dimensioni originali. In caso contrario, ogni ridimensionamento Reimposta la scala al 100%.

*Attributo Microsoft Office Extensions*

**Esempio**

Se la forma viene ridimensionata, le dimensioni originali non verranno archiviate.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 