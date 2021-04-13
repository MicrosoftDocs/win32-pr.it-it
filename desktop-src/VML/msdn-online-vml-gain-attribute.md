---
title: Attributo Gain la
description: Attributo Gain la
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399379"
---
# <a name="vml-gain-attribute"></a>Attributo Gain la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'intensità di tutti i colori in un'immagine. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintassi Tag**

<v: *element* Gain = " *Expression* " >

**Sintassi dello script**

*element* . Gain = "*Expression*"

*espressione* = *elemento*. Gain

**Osservazioni:**

Questo attributo definisce la luminosità del colore bianco, che influisce su tutti gli altri colori. I valori variano da 0 a infinito. Il valore predefinito è 1,0. Il valore 0 non visualizza alcuna immagine. I valori maggiori di 1 alleggeriscono l'immagine e i valori minori di 1 fanno sembrare il grigio.

Questo attributo può essere utilizzato per creare effetti interessanti.

*Attributo standard la*

**Esempio**

L'immagine verrà visualizzata con tutti i colori tendenti verso il grigio.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 