---
title: Attributo Type (estrusione) (la)
description: Attributo Type (estrusione) (la)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872730"
---
# <a name="type-attribute-extrusionvml"></a>Attributo Type (estrusione) (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il modo in cui viene estrusa la forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi Tag**

<o: tipo di *elemento* = " *Expression* " >

**Sintassi dello script**

*element* . Type = "*Expression*"

*espressione* = *element*. Type

**Osservazioni:**

I possibili valori sono:



| Valore       | Descrizione                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | Viene eseguito il rendering dell'estrusione in modo che il centro della proiezione sia infinitamente lontano; in altre termini, le linee di estrusione non sono convergenti, a differenza delle proiezioni prospettiche. Valore predefinito. |
| prospettiva | Viene eseguito il rendering dell'estrusione in un centro di proiezione, che corrisponde al punto di dissolvenza per gli oggetti non ruotati.                                                       |



 

**Attributo Microsoft Office Extensions**

 

 