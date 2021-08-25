---
title: Attributo facet VML
description: Attributo facet VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b1ae12ba31d286f1e029dcd433820e8c50acb05c86a92b2c06e1df50c73a0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681011"
---
# <a name="vml-facet-attribute"></a>Attributo facet VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce il numero di facet usati per descrivere le superfici curve di un'estrusione. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *element* facet=" *expression* ">

**Sintassi dello script**

*element* .facet="*expression*"

*expression* = *elemento*.facet

**Osservazioni:**

Definisce il modo in cui un motore di rendering approssima l'estrusione. Un numero inferiore indicherà una tolleranza di rendering inferiore al motore di rendering e genererà più facet. Numeri più elevati renderanno l'estrusione più sfaccettata. Il valore predefinito è 30.000.

*Microsoft Office Attributo Extensions*

 

 