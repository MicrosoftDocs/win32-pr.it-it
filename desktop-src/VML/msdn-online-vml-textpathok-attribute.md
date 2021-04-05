---
title: Attributo TextPathOK di la
description: Attributo TextPathOK di la
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872569"
---
# <a name="vml-textpathok-attribute"></a>Attributo TextPathOK di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina se verrà visualizzato un percorso di testo. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* textpathok = " *Expression* " >

**Sintassi dello script**

*elemento* . textpathok = "*Expression*"

*espressione* = *elemento*. textpathok

**Osservazioni:**

Se **false**, il percorso non può contenere un percorso di testo. Il valore predefinito è **False**. Questo attributo deve essere impostato su **true** per visualizzare il testo in un percorso.

*Attributo standard la*

**Esempio**

La forma ha un percorso di testo. Viene visualizzato il testo "Hello la" lungo una curva a forma di Smile.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 