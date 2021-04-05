---
title: Attributo Origin (VMLFrame) (la)
description: Attributo Origin (VMLFrame) (la)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729991"
---
# <a name="origin-attribute-vmlframevml"></a>Attributo Origin (VMLFrame) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'origine dell'area di visualizzazione del frame. Proprietà di lettura/scrittura. **VgVector2D**.

**Si applica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintassi Tag**

<v: *element* Origin = " *Expression* " >

**Sintassi dello script**

*element* . Origin = "*Expression*"

*espressione* = *elemento*. Origin

**Osservazioni:**

Il valore predefinito è 0,0. Si noti che l' **origine** funziona solo se il [clip](msdn-online-vml-clip-attribute.md) è **true**. In questo attributo l'origine è definita come angolo superiore sinistro del frame.

*Attributo standard la*

**Esempio**

L'origine dell'area di ridimensionamento è 100PT, 100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 