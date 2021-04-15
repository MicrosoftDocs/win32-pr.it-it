---
title: Attributo on (TextPath) (la)
description: Attributo on (TextPath) (la)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517091"
---
# <a name="on-attribute-textpathvml"></a>Attributo on (TextPath) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce se il testo viene visualizzato. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi Tag**

<v: *element* on = " *Expression* " >

**Sintassi dello script**

*element* . on = "*Expression*"

*espressione* = *elemento*. on

**Osservazioni:**

L'impostazione predefinita è **False**. Questo valore deve essere impostato su **true** per visualizzare il testo in un percorso di testo.

*Attributo standard la*

**Esempio**

Verrà visualizzato il testo sul percorso di testo.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 