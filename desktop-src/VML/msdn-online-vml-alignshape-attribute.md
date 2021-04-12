---
title: Attributo AlignShape di la
description: Attributo AlignShape di la
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339030"
---
# <a name="vml-alignshape-attribute"></a>Attributo AlignShape di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se un'immagine viene allineata a una forma. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* alignshape = " *Expression* " >

**Sintassi dello script**

*element* . alignshape = "*Expression*"

*espressione* = *elemento*. alignshape

**Osservazioni:**

Se **true**, l'immagine utilizzata per creare il riempimento è allineata alla forma. Se **false**, l'immagine utilizzata per creare il riempimento è allineata con la finestra. L'impostazione predefinita è **True**.

*Attributo standard la*

**Esempio**

L'immagine di riempimento affiancata creata da myimage.gif è allineata alla finestra, non alla forma; anche se la forma viene ruotata, l'immagine non lo è.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 