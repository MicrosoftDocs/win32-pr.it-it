---
title: Attributo percorso VML
description: Attributo percorso VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314956452db5a88011a147fd05302483e50cbce3724cf8188068770ec492db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136964"
---
# <a name="vml-path-attribute"></a>Attributo percorso VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Specifica la linea che costituisce i bordi di una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* path=" *expression* ">

**Sintassi dello script**

*element* .path="*expression*"

*expression* = *elemento*.path

**Osservazioni:**

Se una forma contiene [l'elemento Path,](msdn-online-vml-path-element.md) i comandi path dell'elemento Path hanno la precedenza sul valore dell'attributo shape. Vedere **l'argomento** Elemento Path per informazioni dettagliate sul set di comandi usato per i percorsi.

*Attributo VML Standard*

**Esempio**

Un percorso quadrato chiuso è definito nella stringa dell'attributo path. Un punto iniziale viene definito con (usato per il comando moveto) in corrispondenza di 1,1 e viene disegnata una linea con (la lettera "L" usata per la riga di comando a ) dalla posizione iniziale (1,1) agli altri tre punti `m`  `l` (in ordine): 1.200; 200.200; 200,1. La riga viene chiusa con `x` (**close**) e termina con `e` (**end**). Si noti che le coordinate vengono fornite nello spazio delle coordinate relative e che le dimensioni reali sono determinate dalla **larghezza e** **dall'altezza**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo Path](/previous-versions/bb264089(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 