---
title: Attributo ConnectType VML
description: Attributo ConnectType VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76910977c0673500be2e91d9f387b1e61782a1460e5de0d513784caa6f0f1633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999261"
---
# <a name="vml-connecttype-attribute"></a>Attributo ConnectType VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il tipo di punti di connessione utilizzati per collegare forme ad altre forme. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Percorso](msdn-online-vml-path-element.md)

**Sintassi dei tag**

<v: *elemento* o:connecttype=" *espressione* ">

**Osservazioni:**

I possibili valori sono:



| Valore    | Descrizione                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno     | Nessun sito di connessione. Valore predefinito.                                                                                                         |
| rect     | Quattro punti di connessione standard ai punti intermedi dei lati superiore, inferiore, sinistro e destro.                                                   |
| segmenti | Vengono utilizzati i punti di modifica della forma. I punti di modifica sono i punti neri in un editor grafico usati per selezionare parti di una forma. |
| custom   | Matrice personalizzata di percorsi di connessione.                                                                                               |



 

*Microsoft Office Attributo Extensions*

 

 