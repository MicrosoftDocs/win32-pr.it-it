---
title: Attributo HRef (ImageData) (la)
description: Attributo HRef (ImageData) (la)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727431"
---
# <a name="href-attribute-imagedatavml"></a>Attributo HRef (ImageData) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce un URL per un'immagine. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* o:href = " *Expression* " >

**Sintassi dello script**

*element* . href = "*Expression*"

*espressione* = *elemento*. href

**Osservazioni:**

Quando si fa clic sulla forma, il browser caricherà l'URL. L'attributo **href** è simile all'attributo HTML **href** standard degli ancoraggi.

L'uso di questo attributo rende più semplice la creazione di immagini buttonswith in una pagina Web.

Questo attributo viene usato da Microsoft Office solo se un'immagine è stata collegata e incorporata. Microsoft Word dispone di un'interfaccia utente per l'inserimento di immagini in questo modo.

*Attributo Microsoft Office Extensions*

**Esempio**

Quando si fa clic sull'immagine, il browser caricherà il home page Microsoft Corporation.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 