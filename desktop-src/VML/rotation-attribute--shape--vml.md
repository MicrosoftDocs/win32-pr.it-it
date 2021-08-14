---
title: Attributo rotation (Shape)(VML)
description: Attributo rotation (Shape)(VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f73b55b57a7b9d9d7f14cdae4ec71a38a1e38246a4430339db23f35a339430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754136"
---
# <a name="rotation-attribute-shapevml"></a>Attributo rotation (Shape)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'angolo di rotazione di una forma. Proprietà di lettura/scrittura. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *element* style="rotation: *expression* ">

**Sintassi dello script**

*elemento* .rotation="*expression*"

*expression* = *elemento*.rotation

**Osservazioni:**

Il valore in gradi può essere positivo o negativo e i valori maggiori di 360 sono modularizzati in un cerchio di 360 gradi. Gli angoli positivi sono in senso orario. Il valore predefinito è 0.

Si noti che la forma viene riposizionata dopo la rotazione per riflettere le nuove coordinate del rettangolo di selezione.

Si noti anche che per lo scripting **l'attributo di** stile non viene usato e **che Rotation** viene considerato come un attributo diretto della forma.

**L'attributo Rotation** è simile all'attributo **Rotation** HTML standard per gli stili.

*Attributo standard VML*

**Vedere anche**

**Esempio**

Il rettangolo verrà inclinato di 45 gradi.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Esempio di attributo Rotation](/previous-versions/bb264091(v=vs.85)). Richiede Microsoft Internet Explorer 5 o versione successiva.

 

 