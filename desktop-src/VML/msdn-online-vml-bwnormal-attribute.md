---
title: Attributo BWNormal di la
description: Attributo BWNormal di la
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046952"
---
# <a name="vml-bwnormal-attribute"></a>Attributo BWNormal di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la modalità in bianco e nero per i normali dispositivi di output in bianco e nero. Proprietà di lettura/scrittura. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:bwnormal = " *Expression* " >

**Osservazioni:**

Quando [BWMode](msdn-online-vml-bwmode-attribute.md) è impostato su **auto**, questo attributo viene usato per determinare come eseguire il rendering della forma in bianco e nero normale.

Per ulteriori informazioni sui valori di questo attributo, vedere l'argomento [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . Il valore predefinito è **auto**.

*Attributo Microsoft Office Extensions*

**Esempio**

La forma viene elaborata come immagine in scala di grigi per l'output normale in bianco e nero.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 