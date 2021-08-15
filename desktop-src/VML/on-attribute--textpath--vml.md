---
title: Su attributo (TextPath)(VML)
description: Su attributo (TextPath)(VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7b1361bc0600ecca64e252ac25254d26b340cfd34a481de9424017de3381ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345814"
---
# <a name="on-attribute-textpathvml"></a>Su attributo (TextPath)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce se il testo viene visualizzato. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintassi dei tag**

<v: *element* on=" *expression* ">

**Sintassi dello script**

*elemento* .on="*expression*"

*expression* = *elemento*.on

**Osservazioni:**

L'impostazione predefinita è **False**. Questo valore deve essere impostato su **True per** visualizzare il testo in un percorso di testo.

*Attributo standard VML*

**Esempio**

Verrà visualizzato il testo nel percorso di testo.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 