---
title: Attributo ConnectorType di la
description: Attributo ConnectorType di la
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299859"
---
# <a name="vml-connectortype-attribute"></a>Attributo ConnectorType di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Indica il tipo di connettore usato per l'Unione di forme. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Con forme](shape-element--vml.md)

**Sintassi Tag**

<v: *element* o:ConnectorType = " *Expression* " >

**Osservazioni:**

I possibili valori sono:



| Valore    | Descrizione                    |
|----------|--------------------------------|
| Nessuno     | Nessun connettore.                  |
| direttamente | Valore predefinito. Un connettore lineare. |
| gomito    | Un connettore a forma di gomito.     |
| curvo   | Un connettore curvo.            |



 

Questo attributo può essere usato anche da un motore di regole di un editor grafico.

*Attributo Microsoft Office Extensions*

**Esempio**

La forma usa una linea retta come connettore.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 