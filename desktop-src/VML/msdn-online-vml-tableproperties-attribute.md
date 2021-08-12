---
title: Attributo TableProperties di VML
description: Attributo TableProperties di VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050e290bc4b779fec40ebf3ad3fb202b34af23b10f70a0070038c56f5f8ea2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597547"
---
# <a name="vml-tableproperties-attribute"></a>Attributo TableProperties di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Determina le proprietà della tabella. Proprietà di lettura/scrittura. **Integer**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* o:tableproperties=" *espressione* ">

**Osservazioni:**

Usato da Microsoft PowerPoint per le tabelle native. Il valore predefinito è 0. Vengono usati solo i primi tre bit di questo numero intero.

Anche se il valore è archiviato in una forma, l'attributo è utile solo quando la tabella è composta da forme raggruppate. I bit possono essere combinati.

Sono inclusi i valori di bit seguenti.



| bit | Descrizione                              |
|-----|------------------------------------------|
| 1   | Impostare se il gruppo di forme è una tabella.   |
| 2   | Impostare se la forma è un segnaposto.       |
| 3   | Impostare se il testo della tabella è bidirezionale. |



 

*Microsoft Office Attributo Extensions*

 

 