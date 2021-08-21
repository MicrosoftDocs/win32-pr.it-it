---
title: Attributo VML AlignShape
description: Attributo VML AlignShape
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00e1fe8d07fb04c198ced2e2eb50d6ef0e6c020984d2d8cf12a3ca37cf09d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125314"
---
# <a name="vml-alignshape-attribute"></a>Attributo VML AlignShape

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se un'immagine verrà allineata a una forma. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* alignshape=" *expression* ">

**Sintassi dello script**

*element* .alignshape="*expression*"

*expression* = *elemento*.alignshape

**Osservazioni:**

Se **True,** l'immagine usata per creare il riempimento è allineata alla forma. Se **False,** l'immagine usata per creare il riempimento è allineata alla finestra. L'impostazione predefinita è **True**.

*Attributo VML Standard*

**Esempio**

L'immagine di riempimento affiancata creata myimage.gif è allineata alla finestra, non alla forma. anche se la forma viene ruotata, l'immagine non lo è.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 