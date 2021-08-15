---
title: Attributo di guadagno VML
description: Attributo di guadagno VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7b72f1588608f4988731111583e758b0207080eb3e02768a45b58c39071b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057829"
---
# <a name="vml-gain-attribute"></a>Attributo di guadagno VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'intensità di tutti i colori in un'immagine. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi dei tag**

<v: *element* gain=" *expression* ">

**Sintassi dello script**

*elemento* .gain="*expression*"

*expression* = *elemento*.gain

**Osservazioni:**

Questo attributo definisce la luminosità del colore bianco, che influisce su tutti gli altri colori. I valori sono da 0 a infinito. Il valore predefinito è 1,0. Il valore 0 non visualizza alcuna immagine. I valori maggiori di 1 illuminano l'immagine e i valori minori di 1 rendono l'immagine più grigia.

Questo attributo può essere usato per creare effetti interessanti.

*Attributo standard VML*

**Esempio**

L'immagine verrà visualizzata con tutti i colori tendenti al grigio.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 