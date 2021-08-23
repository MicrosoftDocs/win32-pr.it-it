---
title: Attributo VML V
description: Attributo VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbf2f8654d32714d20e9b0c5a36fb939173698749569692120c04b89e84b6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768331"
---
# <a name="vml-v-attribute"></a>Attributo VML V

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce i comandi che costituiscono un percorso. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *element* v=" *expression* ">

**Sintassi dello script**

*elemento* .v="*expression*"

*expression* = *elemento*.v

**Osservazioni:**

Esegue l'override **dell'attributo Path** di una forma. Le coordinate possono essere numeri fissi, numeri relativi o riferimenti alle formule (usando il formato " " dove n è un numero di formula, ad esempio " " fa riferimento alla seconda formula nella @n @2 matrice della formula).

*Attributo standard VML*

**Esempio**

Un rettangolo viene creato usando **l'attributo V.** Si noti che viene usata una lettera minuscola L **(comando lineto)** dopo il primo set di coordinate delimitate da virgole.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 