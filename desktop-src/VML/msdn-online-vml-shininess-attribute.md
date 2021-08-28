---
title: Attributo di luminosità VML
description: Attributo di luminosità VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dea0abba3f605f749e07d247d207a50a6fe7b247ec54bd88024bad3915285e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099051"
---
# <a name="vml-shininess-attribute"></a>Attributo di luminosità VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la concentrazione della luce riflessa su una superficie di estrusione. Proprietà di lettura/scrittura. **VgNumber**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *elemento* lucentezza=" *espressione* ">

**Sintassi dello script**

*element* .shininess="*expression*"

*expression* = *elemento*.brillantezza

**Osservazioni:**

I valori alti (8-10) si approssimano alla luminosità di uno mirror e i valori bassi (2-3) si approssimano a un effetto speckled. I valori da 4 a 7 sono tipici. Le reflection non rispecchiano altri oggetti. vengono riflesse solo le sorgenti di luce di puntina. Il valore predefinito è 5.

*Microsoft Office Attributo Extensions*

 

 