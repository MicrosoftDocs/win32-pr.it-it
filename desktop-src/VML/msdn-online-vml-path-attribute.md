---
title: Attributo Path la
description: Attributo Path la
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872922"
---
# <a name="vml-path-attribute"></a>Attributo Path la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica la linea che costituisce i bordi di una forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *elemento* path = " *Expression* " >

**Sintassi dello script**

*element* . Path = "*Expression*"

*espressione* = *elemento*. Path

**Osservazioni:**

Se una forma contiene l'elemento [path](msdn-online-vml-path-element.md) , i comandi Path dell'elemento Path hanno la precedenza sul valore dell'attributo Shape. Per informazioni dettagliate sul set di comandi usato per i percorsi, vedere l'argomento relativo all'elemento **path** .

*Attributo standard la*

**Esempio**

Un percorso quadrato chiuso viene definito nella stringa dell'attributo path. Un punto iniziale viene definito con `m` (usato per il comando **MoveTo** ) a 1, 1 e viene disegnata una riga con la `l` lettera "L" usata per il comando **LineTo** dalla posizione iniziale (1,1) agli altri tre punti (in ordine): 1.200; 200.200; 200, 1. La riga viene chiusa con `x` (**Close**) e terminata con `e` (**end**). Si noti che le coordinate sono specificate nello spazio delle coordinate relative e che la dimensione reale è determinata dalla **larghezza** e dall' **altezza**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Esempio di attributo path](/previous-versions/bb264089(v=vs.85)). (Richiede Microsoft Internet Explorer 5 o versione successiva).

 

 