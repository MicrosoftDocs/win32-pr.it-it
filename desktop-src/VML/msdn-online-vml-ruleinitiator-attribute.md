---
title: Attributo VML RuleInitiator
description: Attributo VML RuleInitiator
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b015ba3742eda42fd506d955bbc8d2b9d7285999581897952dede665c9eb3361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654961"
---
# <a name="vml-ruleinitiator-attribute"></a>Attributo VML RuleInitiator

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se verrà usato un motore regole. Proprietà di lettura/scrittura. **VgTriState**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* o:ruleinitiator=" *espressione* ">

**Osservazioni:**

Il valore predefinito è **False**. Se il valore è **True,** viene usato un motore regole.

*Microsoft Office Attributo Extensions*

**Esempio**

La forma verrà elaborata da un motore regole.


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 