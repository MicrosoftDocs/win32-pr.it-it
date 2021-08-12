---
title: Attributo VML Limo
description: Attributo VML Limo
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598311"
---
# <a name="vml-limo-attribute"></a>Attributo VML Limo

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Definisce un punto di estensione sul percorso. Proprietà di lettura/scrittura. **Vector2D**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *element* limo=" *expression* ">

**Sintassi dello script**

*element* .limo="*expression*"

*expression* = *elemento*.limo

**Osservazioni:**

Il valore predefinito è "0 0". Le distese limo sono punti sul bordo di una forma che definiscono dove e come una forma può essere estesa da un utente in un editor grafico.

*Attributo standard VML*

**Esempio**

Un punto di estensione limousine viene definito a metà della linea orizzontale.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 