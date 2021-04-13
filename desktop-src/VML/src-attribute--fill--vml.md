---
title: Attributo src (Fill) (la)
description: Attributo src (Fill) (la)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473198"
---
# <a name="src-attribute-fillvml"></a>Attributo src (Fill) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'immagine da caricare per un riempimento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *element* src = " *Expression* " >

**Sintassi dello script**

*element* . src = "*Expression * * *"**

*espressione* = *elemento*. src

**Osservazioni:**

URL di un'immagine da caricare per le compilazioni di immagini e modelli. Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine. Se questo attributo viene visualizzato da solo (ovvero senza **href** o attributo **title** ), l'immagine viene collegata.

*Attributo standard la*

**Esempio**

Viene visualizzata un'immagine affiancata che usa il file myimage.gif come origine.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 