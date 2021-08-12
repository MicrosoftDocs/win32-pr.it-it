---
title: Attributo type (Fill)(VML)
description: Attributo type (Fill)(VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883318c82758178ee9693a1199cb76c5798e351ec809aecb54fe7d0a266d85d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596142"
---
# <a name="type-attribute-fillvml"></a>Attributo type (Fill)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Determina il tipo di riempimento. Proprietà di lettura/scrittura. **VgFillType**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi dei tag**

<v: *element* type=" *expression* ">

**Sintassi dello script**

*element* .type="*expression*"

*expression* = *elemento*.type

**Osservazioni:**

I possibili valori sono:



| Tipo           | Descrizione                                                             |
|----------------|-------------------------------------------------------------------------|
| Solido          | Il motivo di riempimento è a tinta unita. Valore predefinito.                                     |
| gradiente       | I colori di riempimento si fondono in una sfumatura lineare dal basso verso l'alto. |
| gradientradial | I colori di riempimento si fondono in una sfumatura radiale.                    |
| tile           | L'immagine di riempimento è affiancata.                                                |
| pattern        | L'immagine viene usata per creare un motivo usando i colori di riempimento.            |
| frame          | L'immagine viene estesa per riempire la forma.                               |



 

**Attributo standard VML**

**Esempio**

Viene creato un riempimento di sfondo rosso in primo piano e blu usando il modello dell'immagine myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 