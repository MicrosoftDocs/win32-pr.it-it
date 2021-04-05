---
title: Attributo ConnectType di la
description: Attributo ConnectType di la
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117774"
---
# <a name="vml-connecttype-attribute"></a>Attributo ConnectType di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce il tipo di punti di connessione utilizzati per il collegamento di forme ad altre forme. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi Tag**

<v: *element* o:connecttype = " *Expression* " >

**Osservazioni:**

I possibili valori sono:



| Valore    | Descrizione                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno     | Nessun sito di connessione. Valore predefinito.                                                                                                         |
| rect     | Quattro punti di connessione standard in ai punti medi dei lati superiore, inferiore, sinistro e destro.                                                   |
| segmenti | Vengono utilizzati i punti di modifica della forma. I punti di modifica sono i punti neri in un editor grafico utilizzati per selezionare parti di una forma. |
| custom   | Matrice personalizzata di percorsi di connessione.                                                                                               |



 

*Attributo Microsoft Office Extensions*

 

 