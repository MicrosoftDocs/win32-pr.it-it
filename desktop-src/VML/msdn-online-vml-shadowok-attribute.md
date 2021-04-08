---
title: Attributo ShadowOK di la
description: Attributo ShadowOK di la
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046777"
---
# <a name="vml-shadowok-attribute"></a>Attributo ShadowOK di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se verrà visualizzata un'ombreggiatura. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* shadowok = " *Expression* " >

**Sintassi dello script**

*element* . shadowok = "*Expression*"

*espressione* = *elemento*. shadowok

**Osservazioni:**

Se **false**, il percorso non può contenere un'ombreggiatura. Il valore predefinito è **True**. Questo attributo esegue l'override di tutti gli altri attributi shadow nell'elemento padre o **shadow** .

*Attributo standard la*

**Esempio**

La forma non avrà un'ombreggiatura.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 