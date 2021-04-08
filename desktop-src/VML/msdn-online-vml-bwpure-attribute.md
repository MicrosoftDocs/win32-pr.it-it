---
title: Attributo BWPure di la
description: Attributo BWPure di la
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872673"
---
# <a name="vml-bwpure-attribute"></a>Attributo BWPure di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce la modalità in bianco e nero per i dispositivi di output puri in bianco e nero. Proprietà di lettura/scrittura. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:bwpure = " *Expression* " >

**Osservazioni:**

Quando [BWMode](msdn-online-vml-bwmode-attribute.md) è impostato su **auto**, questo attributo viene usato per determinare come eseguire il rendering della forma in bianco e nero puro.

Per ulteriori informazioni sui valori di questo attributo, vedere l'argomento [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . Il valore predefinito è **auto**.

*Attributo Microsoft Office Extensions*

**Esempio**

La forma viene elaborata come immagine a contrasto elevato per l'output puro nero e bianco.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 