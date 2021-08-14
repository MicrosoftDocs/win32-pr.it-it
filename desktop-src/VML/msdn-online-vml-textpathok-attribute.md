---
title: Attributo VML TextPathOK
description: Attributo VML TextPathOK
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2c14d613df36c314dea75275a4d60fe8792d6dea644ef2595422e74a73dc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597455"
---
# <a name="vml-textpathok-attribute"></a>Attributo VML TextPathOK

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se verrà visualizzato un percorso di testo. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *elemento* textpathok=" *espressione* ">

**Sintassi dello script**

*Elemento* . textpathok= "*expression*"

*expression* = *Elemento*. textpathok

**Osservazioni:**

Se **False,** il percorso non può avere un percorso di testo. Il valore predefinito è **False**. Questo attributo deve essere impostato su **True per** visualizzare il testo in un percorso.

*Attributo VML Standard*

**Esempio**

La forma ha un tracciato di testo. Il testo "Hello VML" viene visualizzato lungo una curva a forma di smile.


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



 

 