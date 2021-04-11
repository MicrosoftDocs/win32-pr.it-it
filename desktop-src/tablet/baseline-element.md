---
description: Fornisce le informazioni (x, y) per i punti iniziale e finale della linea di base di un paragrafo nel documento Journal. Lo spazio delle coordinate usato per questi valori è HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225874"
---
# <a name="baseline-element"></a>Elemento Baseline

Fornisce le informazioni (x, y) per i punti iniziale e finale della linea di base di un paragrafo nel documento Journal. Lo spazio delle coordinate usato per questi valori è **HIMETRIC**.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Elementi padre

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuna.

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                      | Valori possibili           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **StartX** | **xs:nonNegativeInteger** | Necessario | Valore X per il punto che contrassegna l'inizio della linea di base. | Qualsiasi numero intero non negativo. |
| **StartY** | **xs:nonNegativeInteger** | Necessario | Valore Y per il punto che contrassegna l'inizio della linea di base. | Qualsiasi numero intero non negativo. |
| **EndX**   | **xs:nonNegativeInteger** | Necessario | Valore X per il punto che contrassegna la fine della linea di base.       | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                               |
|--------------|---------------------------------------------------------------|
| Tipo di elemento | ComplexType [**BaselineType**](baselinetype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                    |
| Nome schema  | Lettore Journal                                                |



 

 

 



