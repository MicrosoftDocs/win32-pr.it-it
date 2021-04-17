---
title: Attributo TableProperties di la
description: Attributo TableProperties di la
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299846"
---
# <a name="vml-tableproperties-attribute"></a>Attributo TableProperties di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina le proprietà della tabella. Proprietà di lettura/scrittura. **Integer**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:tableProperties = " *Expression* " >

**Osservazioni:**

Usato da Microsoft PowerPoint per le tabelle native. Il valore predefinito è 0. Vengono utilizzati solo i primi tre bit di questo Integer.

Anche se il valore viene archiviato in una forma, l'attributo è utile solo quando la tabella è costituita da forme raggruppate. È possibile combinare BITS.

Sono inclusi i seguenti valori di bit.



| bit | Descrizione                              |
|-----|------------------------------------------|
| 1   | Impostare se il gruppo di forme è una tabella.   |
| 2   | Impostare se la forma è un segnaposto.       |
| 3   | Impostare se il testo della tabella è bidirezionale. |



 

*Attributo Microsoft Office Extensions*

 

 