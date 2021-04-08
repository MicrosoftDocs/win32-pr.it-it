---
title: Attributo BWMode di la
description: Attributo BWMode di la
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728295"
---
# <a name="vml-bwmode-attribute"></a>Attributo BWMode di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina come viene eseguito il rendering di una forma per i dispositivi di output neri e bianchi. Proprietà di lettura/scrittura. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:bwmode = " *Expression* " >

**Osservazioni:**

Quando una forma viene stampata su una stampante nera e bianca o visualizzata in una visualizzazione in bianco e nero in un'applicazione, sono possibili diverse opzioni. Per ulteriori informazioni sui valori di questo attributo, vedere l'argomento [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . Il valore predefinito è **auto**.

Se viene specificato **auto** , viene usato [BWNormal](msdn-online-vml-bwnormal-attribute.md) per determinare il comportamento per l'output normale nero e bianco e [BWPure](msdn-online-vml-bwpure-attribute.md) viene usato per determinare il comportamento per l'output puro nero e bianco.

*Attributo Microsoft Office Extensions*

**Esempio**

La modalità nero e bianco della forma è **auto**.


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 