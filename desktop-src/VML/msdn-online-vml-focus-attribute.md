---
title: LA-attributo attivo
description: LA-attributo attivo
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047339"
---
# <a name="vml-focus-attribute"></a>LA-attributo attivo

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il centro di un riempimento sfumato lineare. Proprietà di lettura/scrittura. **VgFraction**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *elemento* Focus = " *Expression* " >

**Sintassi dello script**

*element* . Focus = "*Expression*"

*espressione* = *elemento*. Focus

**Osservazioni:**

Definisce la posizione iniziale del centro della Blend. I valori sono compresi tra 100% e-100%. Il valore predefinito è 0. Un valore 100% (o-100%) Sposta lo stato attivo in modo da invertire la direzione della sfumatura (influisce sul **colore** e **color2**). Il valore 50% modificherà la Blend in modo che il **colore** sia a entrambe le estremità e **color2** al centro. Il valore-50% modificherà la Blend in modo che **color2** sia a entrambe le estremità e il **colore** sia al centro.

*Attributo standard la*

**Esempio**

Lo stato attivo sfumato del riempimento viene spostato in modo che il rosso (**colore**) sarà una banda al centro della forma e che la parte superiore e inferiore sarà blu (**color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 