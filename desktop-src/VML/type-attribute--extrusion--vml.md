---
title: Attributo tipo (estrusione)(VML)
description: Attributo tipo (estrusione)(VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14c3b69aa4156cbd94bb8598caa80ccd92721574daafe074486eb293059cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057585"
---
# <a name="type-attribute-extrusionvml"></a>Attributo tipo (estrusione)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce la modalità di estrusione della forma. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Estrusione](msdn-online-vml-extrusion-element.md)

**Sintassi dei tag**

<o: *element* type=" *expression* ">

**Sintassi dello script**

*element* .type="*expression*"

*expression* = *elemento*.type

**Osservazioni:**

I possibili valori sono:



| Valore       | Descrizione                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | Il rendering dell'estrusione viene eseguito in modo che il centro della proiezione sia all'infinito lontano; ovvero le linee di estrusione non convergono (a differenza delle proiezioni prospettica). Valore predefinito. |
| prospettiva | Il rendering dell'estrusione viene eseguito fino a un centro di proiezione, che corrisponde al punto di estrusione per gli oggetti non tosati.                                                       |



 

**Microsoft Office Attributo Extensions**

 

 