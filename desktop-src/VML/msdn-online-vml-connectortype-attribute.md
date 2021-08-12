---
title: Attributo ConnectorType di VML
description: Attributo ConnectorType di VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a552324582729c74ae87c9fcf1cd512334423bb84c43992f265c0b47fffcd98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601974"
---
# <a name="vml-connectortype-attribute"></a>Attributo ConnectorType di VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Indica il tipo di connettore usato per unire le forme. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Forma](shape-element--vml.md)

**Sintassi dei tag**

<v: *elemento* o:connectortype=" *espressione* ">

**Osservazioni:**

I possibili valori sono:



| Valore    | Descrizione                    |
|----------|--------------------------------|
| Nessuno     | Nessun connettore.                  |
| Dritto | Valore predefinito. Un connettore diritto. |
| Gomito    | Connettore a forma di gomito.     |
| Curva   | Connettore curvo.            |



 

Questo attributo può essere usato anche da un motore regole di un editor grafico.

*Microsoft Office Attributo Extensions*

**Esempio**

La forma usa una linea retta come connettore.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 