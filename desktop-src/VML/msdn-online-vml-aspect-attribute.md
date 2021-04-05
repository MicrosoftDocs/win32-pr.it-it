---
title: Attributo aspect la
description: Attributo aspect la
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728335"
---
# <a name="vml-aspect-attribute"></a>Attributo aspect la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Specifica il modo in cui verranno mantenute le proporzioni dell'immagine di riempimento. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintassi Tag**

<v: *elemento* aspect = " *Expression* " >

**Sintassi dello script**

*element* . aspect = "*Expression*"

*espressione* = *elemento*. aspect

**Osservazioni:**

I possibili valori sono:



| Valore   | Descrizione                           |
|---------|---------------------------------------|
| ignore  | Ignorare i problemi di aspetto. Valore predefinito.        |
| atleast | Le dimensioni dell'immagine sono pari almeno alla **dimensione**. |
| atmost  | L'immagine non è più grande della **dimensione**.     |



 

*Attributo standard la*

**Esempio**

L'immagine che compone il riempimento è maggiore o uguale a una dimensione di 10 punti per 10 punti.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 